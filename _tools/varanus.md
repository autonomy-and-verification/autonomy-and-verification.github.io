---
layout: tool
title: "Varanus"
blurb: "A runtime verification toolchain called Varanus that interfaces with a robotic system, interprets its behaviour, and checks it against a formal specification written in CSP."
author: "Matt Luckcuck"
---

We have built a new runtime verification toolchain called Varanus to interface with the MASCOT system, interpret its behaviour, and check it against the specification. The specification is written in the formal specification language CSP, which is mathematically-based and amenable to a variety of formal methods -- in this case, exhaustive model checking.

 The toolchain currently performs offline verification, by processing logs of system updates. The current version of the MASCOT system does not yet produce the information required to monitor the safety properties.

This runtime verification approach is effective at bridging the reality gap between design-time assumptions and run-time environments; which is especially useful for robotic systems, because they operate in the real-world. The monitoring is based on the system’s safety requirements, therefore providing traceability of these properties into a system component.


## Links

* [Varanus Github](https://github.com/autonomy-and-verification-uol/varanus)<i class="fas fa-external-link-alt"></i>
