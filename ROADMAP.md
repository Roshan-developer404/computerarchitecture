# Roadmap

The current release focuses on a useful, self-contained first learning journey. Future contributions should be tied to a clear student learning outcome.

## Next high-value improvements
- Add a transistor-level CMOS inverter and NAND/NOR lab with switchable input states.
- Add a complete interactive half-adder/full-adder and ripple-carry adder experiment.
- Add a clocked D-flip-flop/register/Program Counter timing lab.
- Extend the RISC-V subset with BEQ, BNE, SLT, LUI and AUIPC, each backed by reference test programs.
- Add an optional five-stage pipeline simulator with data/control hazards, forwarding and stalls. Keep it separate from the single-cycle model.
- Add cache experiments for direct-mapped and set-associative caches, including hit/miss and average memory access time.
- Add accessible keyboard-only controls, captions and reduced-motion settings to every 3D view.
- Replace generic procedural models with original, optimized glTF assets after checking license and performance budgets.

## Quality gates for new simulator features
1. Define the concept and expected learning outcome.
2. Define the model boundary and what is not being simulated.
3. Add known-answer tests and reference calculations.
4. Make beginner and advanced explanations available.
5. Ensure a 2D or text fallback remains usable.
6. Test on a mid-range laptop and a mobile viewport.
