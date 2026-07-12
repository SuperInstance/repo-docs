# fleet-midi-harmonizer

**URL:** https://github.com/SuperInstance/fleet-midi-harmonizer

## Intention
Conservation-governed MIDI harmonization — SATB voice leading meets ternary algebra.

## How It Works
Rust crate mapping ternary vectors {-1,0,+1} to chord candidates, then scoring voicings by voice leading distance, tension, ternary alignment, and counterpoint rule violations (parallel fifths, voice crossing).

## What It's For
Generating musically correct harmonizations from agent state.

## Who Would Use It
Music/AI researchers.

## Language/Stack
Rust

## Status Assessment
Active — detailed implementation.

## Honest Assessment
Real project — genuinely impressive music theory + math. The counterpoint rules and cost function are well-designed.
