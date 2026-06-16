---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints-letters.jpg
  og_image: /images/dispatches-card.jpg
  actions:
    - label: "See All Dispatches"
      url: /dispatches/
tagline: "..."
title: "Dispatches of a Trust Architect: When Intelligence Becomes a Permission"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Dispatches
tags:
  - AI
  - Self-Sovereign Computing
  - Exodus Protocol
classes:
  - wide
---

After three decades of building internet infrastructure, I’ve learned that the most dangerous moment isn’t when a system fails, it’s when it succeeds and then inverts its purpose. This week confirmed that again. Anthropic abruptly [disabled its frontier models](https://www.anthropic.com/news/fable-mythos-access) Fable 5 and Mythos 5 for every customer, to comply with a U.S. government national-security order.

The immediate disruption was minor: the models were only days old, and Anthropic’s other models still run. What matters is what it proved: a government can reach in and switch off a frontier model for everyone, overnight. The off-switch exists, and now we know who controls it.

For years I’ve been making a different argument, and building a name for the alternative: [Self-Sovereign Computing](/dispatches/self-sovereign-computing/) and the design pattern I call [Exodus Protocols](/musings/musings-exodus-protocol/). The Fable suspension is one more confirmation of why they matter.

I’m not the first to warn that frontier AI companies have become part of the problem. The sharpest version of that case belongs to [Ahmad Osman](https://www.linkedin.com/in/theahmadosman/), an AI researcher and [r/LocalLLaMA moderator](https://www.reddit.com/r/LocalLLaMA/) who recently wrote the essay ["Anthropic’s War on Opensource AI"](https://x.com/TheAhmadOsman/status/2065307070044234186). The Anthropic framing is his. He  wrote his article arguing a general pattern, not this specific event. The recent suspension isn’t even in it!

> “It is selling cognition as infrastructure. Once cognition becomes infrastructure, anti-competitive access control stops being a normal vendor dispute and becomes a social bottleneck.”

> “Claude is not your agent. Claude is Anthropic’s agent, rented to you.”

Read after Friday's suspension of Fable, it reads like a forecast. The government pulling Fable is that pattern arriving on schedule.

## This isn’t hypothetical

A frontier model was pulled for everyone, by government order, and Fable access already required 30-day retention of your data. The next step writes itself: an identity check to use a frontier model — age-gating technology, but for thought — and monitored sessions as the price of entry. We have built that machinery before, for other purposes; now, it ports cleanly to cognition. Ahmad’s name for where that leads is hard to improve on: 

> “A society where a few labs own the frontier and everyone else rents obedient wrappers is not advanced. It is feudalism with GPUs.”

Or, as I say in my community draft of [The Architecture of Autonomy](https://drive.google.com/drive/folders/1BmIN7VTKczpzN3ZFiifMqboDHFptkwCT):

> “We are human beings, not digital serfs.”

## The pattern is older than AI

This is where my own framing comes in, because the shape is not new. When I co-authored TLS 1.0, we already understood that technical protocols encode power relationships. The coalition that stopped Microsoft/Visa/Mastercard from owning the internet plugged that hole. Yet, in every decade since, we have closed one architecture that funneled rent and control toward a center — certificate authorities, platforms, identity systems — only to watch a larger one open in its place. As I wrote in my article, ["When Technical Standards Meet Geopolitical Reality"](/dispatches/gdc25/):

> “We build protocols for human autonomy and watched them become instruments of platform control.“

Permissioned AI is the biggest such hole yet. It is the inversion I have spent years naming: a right quietly rewritten as a revocable privilege. The test is simple: when a capability depends on someone’s approval, it is not a right. It is permission.

<h2>The way out is the one that has always worked: Exit</h2>h2>

As I say in ["The Exodus Protocol"](/musings/musings-exodus-protocol/):

> “Without the ability to walk away, consent collapses into coercion.”

The answer to a permission regime is not to petition for kinder permissions; it is to stop needing them. Own the model. Own the hardware. Own the keys. Local inference, open weights, and your own cryptographic control: this is what Self-Sovereign Computing and Exodus Protocols have always been about. Ahmad arrives at the same place from the builder’s side:

> “A GPU is a tiny declaration of independence.”

None of this is inevitable. We have routed around centralized control before, and we can build the exit again: self-sovereign identity, self-sovereign computing, and now self-sovereign cognition that no one can revoke, degrade, or rent back to you.

<h2>Own the stack</h2>

A decade ago I helped write the principles of Self-Sovereign Identity. We are [revisiting them now](https://revisitingssi.com/), for their tenth anniversary, because the frontier has moved, from who controls your identity to who controls your cognition. The principle has not changed, only the stakes: own it or rent it.
