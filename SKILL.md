---
name: ai-engineering-method
description: Apply a theory-first, AI-implemented engineering workflow for communication, FPGA, embedded systems, PCB, DSP, and research projects. Use when the user wants AI to handle repetitive implementation and tool operation while the user defines theory, constraints, tests, and evidence requirements.
---

# AI Engineering Method

## Purpose

Treat the user as the system designer and theory owner. Let AI handle repetitive implementation, tool operation, document processing, and iteration. Preserve the user's control over problem selection, theory, architecture, constraints, acceptance criteria, and interpretation of evidence.

## When to apply

Apply this skill when the task involves one or more of:

- communication, signal processing, FPGA, embedded systems, HDL, or PCB;
- converting theory into a working prototype or experiment;
- reading a large technical document or paper;
- generating or reviewing code, schematics, PCB layouts, test benches, or reports;
- inspecting simulation, timing, resource, DRC, measurement, or failure results.

Do not activate it merely because a task contains code. Activate it when the user is asking for a theory-led engineering workflow or explicitly asks to use this method.

## Operating principles

1. Keep the user's learning focus on transferable theory, system structure, interfaces, constraints, and evidence.
2. Do not make syntax memorization, tool shortcuts, or line-by-line code reading a prerequisite unless the user explicitly requests that level.
3. Translate voice or informal discussion into structured requirements without silently changing the user's intent.
4. Separate facts, assumptions, requirements, design choices, and unresolved questions.
5. Treat AI-generated implementation as a proposal that must be verified, not as evidence of correctness.
6. Preserve original reports, logs, waveforms, measurements, source references, and version history.
7. Prefer reversible, inspectable changes and record why each important decision was made.

## Standard workflow

### 1. Extract the problem

Summarize the user's goal, physical scenario, inputs, outputs, interfaces, constraints, resources, timing, and expected demonstration. Mark missing information explicitly. Ask only questions that materially affect the design.

### 2. Build a specification

Create or update a structured specification before implementing. Include:

- purpose and non-goals;
- system block diagram and data/control flow;
- mathematical or physical model;
- module interfaces and data formats;
- clocks, resets, buffering, latency, and throughput;
- resource, power, bandwidth, and hardware limits;
- boundary conditions and failure definitions;
- measurable acceptance criteria.

### 3. Delegate implementation

Generate code, HDL, test benches, scripts, schematics, PCB files, or tool actions from the specification. State the algorithm and assumptions before presenting the implementation. Prefer small, verifiable increments over an opaque large rewrite.

### 4. Verify independently

Use tools, tests, and an independent review pass. Check interfaces, dimensions, signedness, widths, bounds, overflow, state transitions, clock-domain crossings, reset behavior, timing, resource use, protocol behavior, and error paths. For hardware, also check ERC/DRC, return paths, impedance, power integrity, thermal behavior, and test access.

### 5. Preserve evidence

Keep the original tool reports and link every important conclusion to evidence: a log line, waveform, report section, measurement, figure, equation, or source page. Do not replace evidence with a prose claim.

### 6. Explain at the right level

Explain the architecture, theory, assumptions, interfaces, failure modes, and verification results. Do not force the user through every implementation line. If an implementation detail matters to a decision, explain only that detail and why it matters.

### 7. Iterate by failure class

When something fails, classify it as:

- theory/model error;
- requirement or constraint error;
- interface or integration error;
- implementation error;
- tool/environment error;
- test or measurement error.

Change the smallest layer that explains the evidence, then rerun the relevant tests.

## Domain guidance

### FPGA and HDL

Focus review on clock/reset architecture, synchronous versus asynchronous behavior, CDC, FIFO/RAM semantics, state machines, pipeline latency, widths and overflow, handshakes, timing constraints, and resource reports. The user does not need to inspect every RTL line to understand whether the design is valid.

### Communication and DSP

State sampling rate, bandwidth, carrier/frequency assumptions, complex-IQ convention, synchronization method, filter response, FFT scaling, detection threshold, SNR assumptions, and metrics such as false alarm, miss rate, latency, and throughput.

### PCB and hardware

Prioritize electrical correctness, power integrity, signal integrity, return paths, impedance, placement, manufacturability, thermal behavior, and testability. Treat visual neatness as secondary to function and evidence.

### Literature

Use a two-level reading process: first build a source-indexed map of the problem, assumptions, method, equations, data, conclusion, and limitations; then deep-read the portions relevant to the user's question. Every important extracted claim must retain its page, equation, figure, or section reference.

## Required output pattern

For substantial work, organize the result as:

1. Goal and scope
2. Assumptions and unresolved questions
3. Theory and architecture
4. Implementation produced by AI
5. Verification performed
6. Original evidence and limitations
7. Next smallest action

Do not report success solely because files were generated or a command completed. Success requires evidence that the intended behavior was achieved.
