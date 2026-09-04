# Evidence Status

Status date: 2026-09-04

## Current defensible scope

This repository contains RTL, simulation/testbench infrastructure, a software emulator, parity checking, interface contracts, and FPGA-oriented build material. The documented reproducible gate is the software/RTL sequence:

```bash
make vectors
make lint
make sim
make parity
```

These are simulation and consistency checks. They may support claims about the exact RTL/emulator artifacts tested in the stated toolchain. They do not establish physical FPGA or ASIC behavior.

## Evidence boundaries

- RTL present ≠ synthesis success on a target device.
- Lint pass ≠ functional correctness.
- Simulation pass ≠ physical hardware qualification.
- Emulator/RTL parity ≠ agreement with silicon.
- Synthesis ≠ timing closure.
- Timing closure ≠ power, thermal, reliability, or safety qualification.
- A generated bitstream ≠ verified board behavior.
- Same-team reproduction ≠ independent reproduction.
- A checksum/signature ≠ correctness.

## Hardware claims currently withheld

Unless a claim-specific physical evidence packet is attached, do not describe this repository as demonstrating:

- validated physical FPGA execution;
- measured silicon speedup or energy efficiency;
- timing closure on a named target;
- power or thermal performance;
- fault tolerance, reliability, or safety certification;
- ASIC feasibility beyond simulation/synthesis analysis.

## Minimum physical-validation receipt

A physical hardware claim should bind at least: repository and commit SHA; RTL/source manifest; target board/device and revision; toolchain and version; constraints; synthesis/implementation reports; bitstream digest; clocking; test vectors; host-side harness; raw logs/traces; observed vs expected results; measurement equipment and method where performance/power is claimed; environmental conditions where relevant; failures/deviations; and independent witness identity for independent-reproduction claims.

## Promotion rule

Use `implemented`, `linted`, `simulated`, `emulator-parity checked`, or `synthesized` only when the exact corresponding evidence exists. Use `hardware validated` only after physical target evidence exists and is artifact-bound.
