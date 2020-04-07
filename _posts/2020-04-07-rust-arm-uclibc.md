---
title: "Rust. ARM. uClibc. Choose any three."
layout: post
---

So one day you wake up and decide you want to use Rust in Linux with [uClibc](https://www.uclibc.org/)
on a slightly niche ARM platform. You look at the handy [Rust Forge](https://forge.rust-lang.org/release/platform-support.html)
and realize your dream platform isn’t supported. What ever will you do??

I have spent the bulk of this year wrestling with that question. A customer
requested the usage of our [Rust services](https://github.com/kubos/kubos)
in a uClibc environment on an [ARM Cortex-M3 platform](https://www.emcraft.com/som/m2s-fg484).
The Rust compiler featured limited support for uClibc targets and a bare metal Cortex-M3 target,
but no support for Linux + uClibc on a Cortex-M3. So began the journey of figuring out how to 
bring up a new Rust target and stumbling along the path to a fully portable executable.

Along the course of this journey I found there was not one single place which listed
the steps or resources I would need to bring up this new target. I ended up taking
20+ pages of notes in Notion as I attempted to carefully document the steps I took
and what I learned along the way. My intent is to translate those pages of notes
into several technically dense posts which can serve as a resource and encouragement
to future travelers on the dusty road of a target bring up