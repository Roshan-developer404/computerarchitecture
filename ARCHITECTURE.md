# Application Architecture

## Static deployment

The platform is intentionally static: HTML, CSS, vanilla JavaScript and Three.js loaded from a CDN. GitHub Pages can host it without a server-side runtime, database or build pipeline.

## Pages

- `index.html`: laptop anatomy and keyboard-to-display educational simulation.
- `cpu-lab.html`: RISC-V single-cycle datapath visualization and bounded instruction interpreter.
- `learn.html`: six-module learning path and selected course slide images.
- `logic-microscope.html`: separate custom 8-bit gate-level teaching microcomputer.

## Simulator boundaries

- Laptop key capture uses the browser Keyboard Events API.
- Internal keyboard scan/EC/host transport is a visual teaching model.
- CPU register, datapath, memory and peripheral state in `cpu-lab.html` are simulated in JavaScript.
- Three.js renders illustrative component geometry; it is not an electrical schematic or a transistor-level SPICE model.
- The gate-level microscope models a separate 8-bit architecture and must not be mistaken for the RV32I datapath.

## Extending the RISC-V model

A safe extension sequence is:
1. Add an instruction definition and operand/immediate decoding.
2. Implement the instruction's datapath behavior.
3. Add the required control-signal selection.
4. Add a test program with known expected register, memory and PC state.
5. Compare the simulator result with a trusted reference such as Ripes.
6. Document unsupported corner cases and update the bounded-subset statement.
