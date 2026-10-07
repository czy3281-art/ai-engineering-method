# Review checklists

## Software and scripts

- Does the implementation match the stated algorithm?
- Are input, output, shape, type, signedness, and units explicit?
- Are capacity, bounds, overflow, timeout, and error paths covered?
- Are loop counts and state transitions correct?
- Are external files, devices, and versions recorded?
- Is there an independent test or reference implementation?

## FPGA and HDL

- Are clock and reset assumptions explicit?
- Are all clock-domain crossings handled?
- Are widths, signedness, saturation, and FFT scaling correct?
- Are FIFO full/empty and RAM read/write semantics tested?
- Are handshakes, back-pressure, latency, and throughput measured?
- Do timing, utilization, power, and pin reports meet the specification?

## PCB and hardware

- Are power rails, decoupling, return paths, and grounding correct?
- Are impedance, spacing, length matching, and layer references appropriate?
- Are RF, analog, clock, digital, and switching-power regions separated appropriately?
- Are connectors, test points, thermal paths, assembly, and repair considered?
- Do ERC, DRC, SI/PI checks, and bench measurements agree?

## Literature

- What exact question does the source answer?
- What assumptions and definitions limit the result?
- Which equation, figure, table, or page supports each important claim?
- What is the baseline and what data was actually measured?
- Which parts are evidence, interpretation, or speculation?
- Can the method be reproduced or adapted to the current project?
