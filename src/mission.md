---
layout: base
title: Mission
description: The mission and goals of the Sendspin project.
---
## Who SendSpin Is For

SendSpin is for anyone who believes their music deserves better than closed ecosystems and proprietary lock-in. Whether you're a DIY audio enthusiast breathing new life into old hardware, a home automation tinkerer building your perfect setup, or simply someone who wants synchronized music across every room without vendor restrictions—SendSpin is built for you.

If you've ever been frustrated that your phone can't talk to your speakers, your display can't show what's playing, or your lights can't pulse to the beat because different companies won't play nice together, SendSpin is your answer.

## What We're Building

SendSpin is an open protocol for the **complete music listening experience**. Not just audio streaming—the whole thing: synchronized playback, rich metadata, album artwork, playback controls, and even music visualization data.

We're building what Apple's AirPlay and Google's Cast should have been: completely open and designed to unleash the creativity of the community rather than lock it down.

### Our Core Goals

**User Sovereignty**: You should control your devices, your data, and your music. Full stop. Open standards make this possible; proprietary protocols make it impossible.

**Complete Experience**: Existing protocols stop at audio streaming. SendSpin orchestrates everything—the e-paper display showing album art, the speakers playing in perfect sync, and the smart lights pulsing to the rhythm.

**Universal Compatibility**: Turn anything into a synchronized music system. ESP32 boards, Raspberry Pis, Android phones, web browsers, even old tablets—if it can connect to a network, it can probably be part of your SendSpin setup.

## Experience Philosophy

### Synchronization: Invisible Perfection

Multi-room audio lives or dies on synchronization, but how you achieve sync matters as much as whether you achieve it.

**The goal**: When you press play, there's a brief pause (≤1 second), then all players start together and stay together. The music sounds identical to a perfectly-clocked reference system. You walk from room to room hearing seamless continuity, not echoes or drift.

**How we get there**:

How a player gets in sync is really up to the player, but for the best ecosystem experience ideally players would use:

- **Sophisticated, inaudible adjustments**: Small constant frame manipulation corrections and continual clock alignments that keep players playing together without anyone noticing. This is the ideal path: sync so good it's invisible.

- **Smart resampling when needed**: If drift occurs, intelligent catch-up/slow-down that resamples audio sequences to match pitch, making corrections imperceptible rather than jarring.

- **Brief pauses as last resort**: If a player falls significantly out of sync, a momentary pause to re-anchor is acceptable—but if this happens frequently, it signals something fundamentally wrong. We surface clear diagnostics to help you fix the root cause (network issues, hardware limitations, configuration problems).

**What we won't tolerate**:

- **Pitch warble**: Rapid, granular sync shifts that make the music wobble
- **Audio distortion**: Sync methods that change how the music sounds versus a reference playback
- **Frequent dropouts**: Rapid frame dropping or regular cut-outs that create audible gaps
- **Sluggish response**: Delays >2 seconds between pressing play and hearing music
- **Truncated tracks**: Never cutting off the beginning (or end) of a track to "catch up"

The measure of success: you forget you're using a networked multi-room system because it just works.

### Graceful Adaptation

Not every device has the same capabilities, and that's fine. SendSpin adapts:

- **Codec flexibility**: FLAC for lossless quality when bandwidth allows, Opus when it doesn't, automatic fallback to PCM if needed
- **Role-based communication**: Speakers only get audio, displays only get metadata and artwork, controllers only get playback commands—no device receives data it can't use
- **Network resilience**: WebSockets for local performance, WebRTC fallback for remote access

- **Manual override**: Sometimes the algorithm doesn't know your quirky hardware. Manual sync offset controls let you fix what automation can't

### Developer-Friendly, Always

SendSpin is designed to be extended, not just used. Every decision favors openness:

- **Open specification**: Fully documented protocol anyone can implement
- **Multiple implementations**: Python, Go, Rust, JavaScript—use what you know
- **Permissive licensing**: Apache 2.0 means commercial use is welcome
- **Living standard**: The spec evolves with community input, not corporate roadmaps

