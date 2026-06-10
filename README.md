# Full Adder — Verilog Implementation & Verification

A 1-bit full adder designed and verified in Verilog with a complete testbench covering all 8 input combinations.

---

## What is a Full Adder?

A full adder is a digital circuit that adds three 1-bit inputs:
- **A** — first input bit
- **B** — second input bit  
- **C** — carry input (from previous stage)

And produces two outputs:
- **Sum** — the addition result
- **Cout** — carry output (to next stage)

---

## Files

| File | Description |
|------|-------------|
| `full_adder.v` | RTL design of the full adder |
| `testbench.v` | Testbench verifying all 8 input combinations |

---

## Truth Table

| A | B | C | Sum | Cout |
|---|---|---|-----|------|
| 0 | 0 | 0 |  0  |  0   |
| 0 | 0 | 1 |  1  |  0   |
| 0 | 1 | 0 |  1  |  0   |
| 0 | 1 | 1 |  0  |  1   |
| 1 | 0 | 0 |  1  |  0   |
| 1 | 0 | 1 |  0  |  1   |
| 1 | 1 | 0 |  0  |  1   |
| 1 | 1 | 1 |  1  |  1   |

---

## Testbench Features

- Tests all 8 possible input combinations
- Reusable `check` task compares actual vs expected outputs
- Prints PASS/FAIL for each test case

PASS: 000 → Sum=0 Cout=0
PASS: 001 → Sum=1 Cout=0
PASS: 010 → Sum=1 Cout=0
PASS: 011 → Sum=0 Cout=1
PASS: 100 → Sum=1 Cout=0
PASS: 101 → Sum=0 Cout=1
PASS: 110 → Sum=0 Cout=1
PASS: 111 → Sum=1 Cout=1
Results: 8 PASSED, 0 FAILED
- Displays final score at the end

### Example Output
