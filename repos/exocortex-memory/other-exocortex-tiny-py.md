# exocortex-tiny-py

## Intention
**The ESP32 is the PLATO terminal. The exocortex is the mainframe.**

## How It Works
```
┌─────────────────────────────── SENSE-THINK-ACT LOOP ───────────────────────────────┐
│                                                                                      │
│    ┌──────┐    ┌─────────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐     │
│    │SENSE │───►│   FORMAT    │───►│  SEND    │───►│ PARSE    │───►│   ACT    │     │
│    │      │    │   DATA      │    │  TO      │    │ RESPONSE │    │          │     │
│    │temp  │    │             │    │ EXOCORTEX│    │

## What It's For
`exocortex-tiny-py` is a **zero-dependency** Python library that lets an ESP32 microcontroller act as a sensor-actuator node controlled by a remote exocortex server. The ESP32 reads sensors, asks the exocortex "what should I do?", and executes the answer.

```
┌─────────────────────────────────────────────────────────────────────┐
│                        THE EXOCORTEX MODEL

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Python

## Status Assessment
Documented with tests, API docs, and installation guide (841 line README).

## Honest Assessment
Well-documented (841 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/exocortex-tiny-py](https://github.com/SuperInstance/exocortex-tiny-py)*
