# Security Policy

`t81-hardware` is experimental hardware/RTL research. No safety-critical, security-critical, or production hardware assurance is implied.

## Reporting

Prefer GitHub private vulnerability reporting when enabled. If no private channel is available, open a minimal public issue requesting a private contact route and omit exploit details, secrets, device credentials, proprietary bitstreams, and sensitive logs.

Reports should identify the exact commit, affected RTL/module/script, simulator or FPGA toolchain/version, target device where applicable, reproduction procedure, inputs/vectors, and observed behavior.

## Security-sensitive surfaces

Treat HDL parsers/toolchains, generated artifacts, build scripts, downloaded ecosystem data, host/FPGA interfaces, firmware/bitstreams, and test vectors from untrusted sources as untrusted input. CI, lint, simulation, parity tests, synthesis, or bitstream generation do not establish absence of vulnerabilities.

Physical safety and fault-tolerance claims require separate engineering validation. See `EVIDENCE_STATUS.md`.
