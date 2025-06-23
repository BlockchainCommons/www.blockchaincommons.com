---
tagline: "Economic Agency is the Foundation for Human Rights"
title: "Musings of a Trust Architect: Architecting Trust in Software Releases"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - article
tags:
  - Musings of a Trust Architect
---

When can you trust a software release? How do you know that a software repo is safe, that it represents the intent of its creators? On the 20th anniversary of Git, these questions are more important than ever.

Obviously, Git lays the foundation for trust in software releases with its ability to sign commits, but the trust of the system is unfortunately shallow. Untrusted content can be merged into a trusted repo, commit histories can be rewritten, and trust can't be reliably extended into the future. These are crucial issues to solve if we are trusting software that originates in Git ... and some pretty crucial software originates with Git, from [Microsoft's vscode](https://github.com/microsoft/vscode) or the [OpenSSL project](https://github.com/openssl/openssl) to the [vue.js framework](https://github.com/vuejs/core). Which is what led me to the design of the Open Integrity system. Though Git may _look_ like to the average user like it offers a strong level of trust, it's a dangerous mirage. Open Integrity makes repo trust a reality.

<center>
  <img src="/images/openintegrity-darkbg.png">
</center>

Open Integrity is still built with Git, meaning that it can be used on GitHub, GitLab, or whatever other Git tool that you prefer. There are no additions required other than the Open Integrity scripts themselves. However, Open Integrity makes trust the default rather than an add-on, establishing a root of trust when a repo is created, defending it against inappropriate additions, and extending that trust to new users and new keys as a project evolves. 

Beyond that, Open Integrity's root of trust can also be used as a DID (decentralized identifier) identity, supporting [self-sovereign identity](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/) for a user or a project. But taking advantage of that might be the next step. For the moment, let me dive a bit further into the problems of Git's current trust framework and how I designed the architecture of Open Integrity to resolve them.

## A Problem of Trust

The foundation of trust in Git is signing commits with a signing key that is registered with a Git account, but that turns out to be a fragile level of trust because it leaves a number of loopholes.

* ___Signing isn't required.___ Even if an account has a legitimate signing key, use of that key isn't required. Even if a Git hosting service enforces commit signing, unsigned commits can typically still be merged from branches.

* ___Merging doesn't guarantee signatures.___ Generally, merging offers one of the biggest gaps in signing security. It's not just that merged commits can be unsigned, but that a branch can be deleted after merging, leaving no trace as to whether its commits were signed or not.

Things don't necessarily get better when signing actually occurs.

* ___Repo origin can't be verified.___ Though you can verify signed commits belong to the person who currently controls a repo, there's no way to verify that they haven't illegitimately taken over the repo since its inception.

* ___Chain of trust functionality is non-existant.___ On the flipside, there's no way to show a legitimate transfer of authority between a repo's originator and its current controller.

* ___Key revocation is weak.___ Though keys can be manually revoked, there's no way to automatically do so, and there are no warnings if a revoked key was used for signing.

* ___History can be rewritten.___ Finally, Git includes a [purposeful tool](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History) to allow you to rewrite commit history: editing commit messages, rebasing at a large scale, and even removing or changing files! This will change SHA-1 checksums, but as with other dangers here, there's inadequate messaging to warn of this issue.

## Solving the Problems

Solving Git's trust issues are relatively easy in theory:

1. Repo ownership needs to be cryptographically provable back to a repo's origin.
2. Signing needs to be required for commits and merges alike.
3. Commit history needs to be irrevocable.
4. Strong warnings are needed when these conditions aren't met.

However, nothing is ever that simple in practice. To practically solve the problems required designing an Open Integrity architecture that resolved each of the highlighted problems:
    
| Problem | Solution |
|---------|----------|
| Unverified Origin | Inception Commit |
| Unverified Transfer | Trust Transition Commit |
| Key Revocation | Trust Transition Commit<br>Improved Logging |
| Signing Not Required | Scripted Functions<br>Defined Settings |
| Merging Issues | Scripted Functions<br>Data Preservation<br>Defined Settings |
| History Issues | Improved Logging<br>Defined Settings |

Here's how each of these architectural elements work:

***Inception Commit.*** An inception commit is the first commit made to a repo. It locks the repo's inception (initial) key with an empty commit, and so secures the repo with both the SSH signature and a SHA-1 hash that's hard to purposefully collide because of the minimalism of the commit.

***Trust Transition Commit.*** Any authorized key can be used to generate a trust transition commit, which is another zero-sized commit. Additional, trusted keys can be added, and keys can also be revoked. This allows both keys and team members to change over the course of a project, which is crucial for an open-source or large-scale project. The first trust transition commit is done with the inception key; after that any authorized key can be used.

***Improved Logging.*** Many of the protections of Open Integrity arise from scripts that incorporate extensive logging, ensuring that users can see that all security measures are being met. This is done with Git commit messages and with `git note`.

As an example, here is what the commit logging looks like for an inception commit, a trust transition commit, and a key revocation:

*Inception Commit:*
```
🔹 Commit: #a3306ef [🏁 Inception Commit] (Signed ✅)
    ├─ Message: "Initialize repository and establish a SHA-1 root of trust"
    ├─ Signed by: @a61TkTtL... (🏁 Alice using Device 1 <alice@example.com>)
    ├─ Empty: true (no files added)
    ├─ SHA-1 Protection: Constrained content + SSH signature
└─ Verification: Platform-independent
```

*Trust Transition Commit:*
```
🔹 Commit: #b24d9c1 [🔑 New Allowed Commit Signers File] (Signed ✅)
    ├─ Message: "Added second device key for Alice"
    ├─ Signed by: @a61TkTtL... (🏁 Alice using Device 1 <alice@example.com>)
    └─ New Authorized Commit Signers:  
        - 🏁 Inception Key explicitly not included for future commits
        - + @a61TkTtL... (Alice using Device 1 <alice@example.com>)  
        - + @f84PmWnY... (Alice using Device 2 <alice@example.com>)
```
*Key Revocation:*
```
🔹 Commit: #c3d7f12 [🔄 Key Rotation: Removed Alice's Second Device] (Signed ✅)
    ├─ Message: "Revoked second device key"
    ├─ Signed by: @f84PmWnY... (Alice using Device 2 <alice@example.com>)
    ├─ Authorized Commit Signers changed:
        - 🗑️ @f84PmWnY... (Alice using Device 1 <alice@example.com>) is no longer authorized.
        - @f84PmWnY... (Alice using Device 2 <alice@example.com>)
        - @b73RkKpQ... (Bob using Work Laptop <bob@example.com>)  
        - @c58XmWpL... (Charlie using Home PC <charlie@example.com>) 
```
The commits also clearly show when something is done that violates the basic precepts of Open Integrity. For example:
```
    ├─ 🚨 ERROR: Commit was signed using a previously revoked key!
```

***Scripted Functions.*** Logging and the other protections of Open Integrity are available through scripts and one-line "snippet" scripts that can run from aliases. They replace the bare `git` functions with ones that ensure that each commit or merge meets all the Open Integrity requirements. For example, here's a `git merge` alias:
```
git merge feature-branch --verify-signatures \
    --require-author-signature \
    --require-committer-authorization
```

**Defined Settings.** Git allows settings for repos and workflows; securing these settings can improve the security of repos. ["Enforcing Signed Commits and Pull Request Requirements in GitHub"](https://github.com/OpenIntegrityProject/core/blob/main/docs/Enforcing_Signed_Commits_And_PRs_GitHub.md) describes how GitHub makes use of these settings; similar functionality is available elsewhere in the Git ecosystem.

**Data Preservation.** Logging, aliases, and settings together ensure the preservation of some data related to a merge. As the following commit shows, information such as an author's key is preserved when a merge occurs, along with information that the committer verified the original signature.
```
🔹 Commit: #fa34d76 [🔀 Merge Commit with Verified Author] (Signed ✅)
    ├─ Message: "Merge feature-branch: Added authentication layer"
    ├─ Committer: @c58XmWpL... (Charlie using Home PC <charlie@example.com>)
    ├─ Author: @e83TkLqM... (Eve using Dev Machine <eve@example.com>)
    ├─ Author Signature: Verified ✓ (signed 2024-02-10T15:30:00Z)
    ├─ Committer Authorization: Verified ✓ (in allowed_signers since 2024-01-15)
    └─ Signatures stored: ./config/verification/signatures
```    
The original author's signature is not currently preserved due to the complexity of doing so. Working to preserve the signature without having to keep the branch around forever remains on the TODO list for Open Integrity.

## Using Open Integrity Now

Open Integrity is available at the [OpenIntegrityProject repo](https://github.com/OpenIntegrityProject). Though it's still in development, you can get started with it right now.

You should do so if you have a use case for Open Integrity such as:

* You're developing or releasing software through Git that holds sensitive information (such as a digital-asset wallet, a healthcare app, or even a web browser).
* You're developing or releasing software through Git that might be used by people or companies that also hold sensitive data (such as financial or medical companies), even if your app does not.
* You're developing or releasing software that requires any level of trust from its users.
* You have a team of developers that changes over time.

The docs at the Open Integrity repo include a more extensive [Problem Statement](https://github.com/OpenIntegrityProject/core/blob/main/docs/Open_Integrity_Problem_Statement.md) that goes beyond what's in this article, but the most important file might be the [setup_git_inception_repo.sh](https://github.com/OpenIntegrityProject/core/blob/main/src/setup_git_inception_repo.sh) script, which will create a new Open Integrity repository for you. If you want to better understand how it works under the hood, see [One Liners](https://github.com/OpenIntegrityProject/core/blob/main/docs/Open_Integrity-CLI_One_Liners.md), which also documents step-by-step how to setup and use an Open Integrity repo. Future plans can be found in the [Project Roadmap](https://github.com/OpenIntegrityProject/core/blob/main/ROADMAP.md).

Give it [a try](https://github.com/OpenIntegrityProject/core/blob/main/docs/Open_Integrity-CLI_One_Liners.md), and if you have questions, please feel free to [open an issue](https://github.com/OpenIntegrityProject/core/issues) or [start a conversation](https://github.com/orgs/OpenIntegrityProject/discussions).

I've been working on Open Integrity for about a year now. I started this work because I thought the promise of trust implicit in Git was extremely important for software design and release, but that it needed improvement. I hope you'll agree and find the improvements worthwhile!
