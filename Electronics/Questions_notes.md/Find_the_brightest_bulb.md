2025/09/25

## Example 1: Find the brightest bulb

[Back](../README.md)

### Schematic
---

*Add schematic here*

#### tl;dr
---
$$ R_{component} / R_{branch} \approx P $$

#### Description
---
This circuits has two parallel branches, with 3 bulbs per branch.
The only information given is the resistance of the buibs.
- Branch A
    - 3Ω, 5Ω, 4Ω
- Branch B
    - 10Ω, 2Ω, 1Ω

#### Analysis
---
- There are two branches with bulbs in series.
- In a series circuit the current (I) is the same through all components.
- The power (P) dissipates proportionally to the resistance (R).
- So the bulb with the greatest resistance in each branch will be the brightest buld in it's own branch.
- In a parallel circuit, the voltage (V) is the same across all branches.
- The total resistance (R) of each branch determines the current flowing through it
    - $I = V/R_{branch}$
- A branch with a lower total resistance will have a higher current
- Given the bulb with the highest resistance in each branch will be the brighest. We only need concern ourselves with the 5Ω bulb of brach A and the 10Ω bulb of branch B

#### Calculations
---
Branch resistace
- A = $3Ω + 5Ω + 4Ω = 12Ω$
- B = $10Ω + 2Ω + 1Ω = 13Ω$

Branch current

The voltage across parallel branches is the same.
- A = $V/R_A = V/12$
- B = $V/R_B = V/13$

$12 < 13$ so branch A has more current.

Power of the brightest bulbs
 - The resistance of the brightest bulb / the resistance of the branch squared

Branch A
$$ P_{5Ω} = I^2_A \times 5 = (V/12)^2 \times 5 = V^2/144 \times 5 = 5V^2/144 = 0.0347 $$

Branch B
$$ P_{10Ω} = I^2_B \times 10 = (V/13)^2 \times 10 = V^2/169 \times 10 = 10V^2/169 = 0.0592 $$
$0.0592 > 0.0347$ so the 10Ω buld receives more power and therefore is the brightest.