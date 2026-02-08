# GhostWire Audio
*A one-person company for understanding real-time sound systems*

GhostWire Audio is an open-source learning and research project focused on how audio software actually works under the hood.

The whole thing is a long-term engineering project exploring the systems that make sound software possible — buffers, timing, threading, DSP, and architecture.

The goal is simple: build real tools while learning how real software is designed.

---

## What This Project Is

Most audio tools hide their machinery behind polished interfaces.  
GhostWire exists to expose that machinery and make it understandable to the aspiring indie developer.

Here, sound is treated as a systems programming problem:

- How does audio move through memory?
- What makes real-time code safe?
- How do you change parameters without glitches?
- How do small DSP blocks become full software instruments?

Instead of starting with features, this project starts with infrastructure.

---

## Project Structure

GhostWire is split into multiple repositories, each representing a different layer of the same system.

### `gw-core`
The core audio engine.

*In-progress*

A real-time-safe C++ audio engine and DSP framework responsible for:
- audio buffers
- processing nodes
- DSP graphs
- parameter handling
- offline rendering
- platform audio backends

Everything else in GhostWire depends on this (except for MicroDSP, which throws in some JUCE as well).

---

### `gw-testlab`
The measuring instruments.

*Conceptualized, but hasn't begun*

Tools for testing, visualizing, and validating DSP behavior:
- signal generation
- FFT analysis
- performance benchmarking
- regression testing

This ensures systems behave correctly, not just audibly.

---

### `spectral-ghost`
The public prototype.

*Conceptualized, but hasn't begun*

An experimental plugin built on top of the engine.  
This is where infrastructure becomes a creative tool.

The purpose is not just to make an effect, but to demonstrate how the underlying systems translate into sound.

---

### `ghostwire-docs`
The notebook.

Architecture explanations, design decisions, and long-form writeups documenting what is being learned while building the system.

If the code shows *how*, this explains *why*.

---

## Philosophy

GhostWire follows a few guiding ideas:

**Real-time safety matters**  
Audio systems cannot pause, stall, or wait. The constraints are strict and force careful design.

**Systems over features**  
Understanding structure scales further than collecting tricks.

**Transparency over magic**  
Readable code is more valuable than clever code.

**Learning in public**  
Mistakes and revisions are part of the process, not something to hide.

---

## What You Can Expect

This project evolves over time.  
APIs will change. Architectures will be refactored. Early code will be replaced.

The goal is not perfection — the goal is understanding.

---

## Who This Is For

- Developers curious about audio programming
- Programmers wanting real-time systems experience
- People who like seeing how software works internally
- Anyone interested in the intersection of math, sound, and architecture

---

## Status

Active and evolving.  
Nothing here should be considered stable yet.

---

## License

Unless otherwise specified, repositories are released under the MIT License.

---

If you are reading this, you are seeing the project in progress — which is exactly the point.
