# Obligatio AI Time-Travel Debugger

Overview

This project implements an offline, AI-assisted debugging system for the Obligatio game engine.
It records gameplay sessions, tracks inputs and state transitions, and enables post-mortem root cause analysis using a local LLM via Ollama.

Key Features

- Frame-accurate gameplay recording
- Selective method instrumentation
- State snapshots and heap summaries
- User-defined bug time window
- Natural language symptom descriptions
- Deterministic backward causal analysis
- AI-generated reproduction steps and fixes
- Fully offline operation

System Architecture

Game
 ↓
Instrumentation
 ↓
Event Recorder
 ↓
Snapshots / Heap Sampler
 ↓
Analysis Engine
 ↓
Ollama (LLM)
 ↓
Bug Report + Repro

Recording Model

- Append-only binary event logs
- Indexed by timestamp and frame
- Ring-buffered for memory safety
- Compression enabled

Debugging Workflow

1. User plays game
2. Bug occurs
3. Game closes
4. Debug UI opens
5. User selects bug time window
6. User describes symptom
7. System analyzes session
8. AI produces diagnosis and repro

Performance Strategy

- Sampling over tracing
- Toggleable verbosity
- Snapshot diffing
- Bounded analysis windows
- Minimal allocations

AI Philosophy

The AI does not guess.
The system proves.
The AI explains.

Development Phases

1. Event recording
2. Input & state capture
3. Failure detection
4. Backward analysis
5. AI integration
6. Reproduction automation

Status

🚧 In active development

Final words (important)

What you’re building is not “AI debugging”.
It’s a professional-grade observability system with an AI brain attached.

That’s why this will actually work.