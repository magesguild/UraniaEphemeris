# The Inka Khipu Field Manual
## A Hands-On Guide to Yupana Arithmetic and Khipu Records

**Basin Game Studios · Mage's Guild Psychonautics**  
*English edition · 2026 · MIT License*

> This article is a web edition of the supplied *Educator's Field Manual: The Inka Khipu Arcade & Somatic Compute System*. It preserves the manual's teaching model while labeling its modern pedagogical system as a reconstruction and adaptation, not as a settled account of ancient Andean practice.

## 1. Purpose and pedagogical foundations

The manual's objective is to teach positional decimal arithmetic, spatial matrix decomposition, and deterministic logic without relying on abstract memorization, external data stacks, or electronic computation.

Its central model is a unified, tactile information-processing architecture:

- **The Yupana** is the active workspace: a physical board where counters move through cup receptacles as a calculation proceeds.
- **The Khipu** is the durable record: a physical cord archive into which a settled state may be recorded using positional and knot features.
- **The clock step** is a deliberate manual pass across the board. The operator places a state, then applies local rules—fusion, avalanche, and unweaving—until the board settles.

The manual calls this **somatic computing**: the hands, board, counters, and observer together form the computational apparatus. That is a modern teaching lens. It is useful because it makes state and transformation visible, but it should not be mistaken for proof that historical khipukamayuq practice used this exact vocabulary or procedure.

### Learning outcomes

By completing the module, a student should be able to:

1. Express any decimal number from 0 through 9,999 on a physical four-cup grid, using no more than three counters per row in the rested form.
2. Perform addition and subtraction through fusions, avalanches, and unweaving rather than memorized carry and borrow algorithms.
3. Explore multiplication as spatial loom shifts and division as fair-share allocation.
4. Explain how a tactile, non-silicon system can process a deterministic workload.

## 2. Materials and physical setup

For each student or pair:

1. One Yupana board: five rows by four geometric columns.
2. Thirty to forty counters: quinoa beans, dry corn kernels, small stones, or tokens.

An egg carton or a drawn 5 × 4 grid is enough for a first lesson. No cards, paper stacks, or external state trackers are required for the board exercises.

### Board topology

Each row contains four cups valued **[5], [3], [2], [1]**. The vertical rows represent powers of ten:

| Row | Place | Value |
|---:|---|---:|
| 0 | Units | 10⁰ = 1 |
| 1 | Tens | 10¹ = 10 |
| 2 | Hundreds | 10² = 100 |
| 3 | Thousands | 10³ = 1,000 |
| 4 | Ten-thousands | 10⁴ = 10,000 |

The four horizontal cup values form each digit. For example, a 7 in the hundreds row is a counter in [5] and a counter in [2], giving 7 × 100 = 700.

## 3. Unit 1: digit representation

To represent a decimal digit, place counters in cups whose values sum to that digit. The manual's **Golden Rule** is:

> Always place counters in the largest available cup that fits the remaining value.

In the rested form, this keeps every digit to at most three counters.

| Digit | Cup combination | Counters |
|---:|---|---:|
| 0 | empty row | 0 |
| 1 | [1] | 1 |
| 2 | [2] | 1 |
| 3 | [3] | 1 |
| 4 | [3] + [1] | 2 |
| 5 | [5] | 1 |
| 6 | [5] + [1] | 2 |
| 7 | [5] + [2] | 2 |
| 8 | [5] + [3] | 2 |
| 9 | [5] + [3] + [1] | 3 |

To set 382, place 3 + 8 + 2 in the hundreds, tens, and units rows respectively. To set 1,509, place 1 in thousands, 5 in hundreds, leave tens empty, and place 9 in units.

## 4. Unit 2: addition and the clock-step avalanche

Addition begins physically. Set the first number, then place the second number's counters into the corresponding rows without carrying immediately. The board is intentionally allowed to enter an unsettled state.

On the clock step, sweep from the units row upward and apply local rules:

1. Two [1] counters fuse into one [2].
2. A [1] and a [2] fuse into one [3].
3. A [2] and a [3] fuse into one [5].
4. When two [5] counters occupy a row, they fuse and avalanche upward as one [1] counter in the next row. The current [5] cup clears to zero.

### Addition procedure

1. Set **A** according to the Golden Rule.
2. Take the counters for **B**.
3. Drop them into the corresponding cups and rows.
4. Sweep from 10⁰ upward, resolving fusions and avalanches until every row is rested.

For example, 247 + 385 is performed by setting 247, dropping in 385, and clock-stepping. The target settled state is **632**: hundreds [5] + [1], tens [3], units [2].

## 5. Unit 3: subtraction and unweaving

Subtraction removes counters directly. When a row lacks the counter needed for the subtrahend, unweave a counter from the next higher row:

> Remove one [1] counter from the 10ⁿ⁺¹ row and replace it with two [5] counters in the 10ⁿ row.

This expresses 10 as 5 + 5 in the lower place. Then remove the requested amount.

### Subtraction procedure

1. Set the minuend **A**.
2. Identify the subtrahend **B** by digit and place.
3. Remove counters from the highest relevant row downward.
4. If a cup lacks a required counter, unweave from above and continue.

Example: for 1,204 − 531, unweave the thousands [1] into two hundreds [5] counters, remove 531, and settle at **673**.

## 6. Unit 4: multiplication as a loom

The manual treats the vertical rows as loom rails. Multiplication is built from partial patterns rather than memorized times tables:

- ×1 replicates a pattern in its row.
- ×2 doubles the pattern.
- ×3 triples the pattern.
- ×5 shifts the pattern upward one row, corresponding to ×10, with the cup pattern resolved by the local rules.
- Multiplication by tens or hundreds shifts the whole pattern upward by one or two rows.

Place the partial products, then perform one clock step. The worksheet example is **64 × 23 = 1,472**: decompose 23 as 20 + 3, shift and place the ×2 component, place the ×3 component, and settle the combined board.

## 7. Unit 5: division and Ayni fair-share allocation

The manual presents division as the inverse of the multiplier loom. It uses **Ayni**, reciprocal exchange or fair-share distribution, as the pedagogical frame: a communal total is repeatedly partitioned into equal allotments.

### Four-step protocol

1. **Board setup:** place the dividend on the main grid and keep the divisor as a reference pattern.
2. **Test capacity:** scale the divisor to the highest occupied tier and test whether it fits.
3. **Harvest and allot:** subtract one full divisor unit and record one quotient count at that tier.
4. **Step down:** unweave remaining counters toward lower tiers and repeat until the units are complete.

The manual works through **4,800 ÷ 32 = 150** and **1,472 ÷ 23 = 64**. In each case, division is a sequence of visible tests, subtractions, unweavings, and quotient records rather than an invisible symbolic operation.

## 8. Unit 6: the Khipu archive

When a calculation settles on the Yupana, the manual proposes committing its state to a pendant cord. The following is the manual's teaching baseline, not a complete account of khipu variation:

| Feature | Teaching use in this manual |
|---|---|
| Single knot (S) | Thousands and higher places |
| Long knot (L) | Tens and hundreds; finger-turn count gives the digit, e.g. L7 |
| Figure-eight knot (E) | A 1 in the units place |
| Empty cord space | A zero placeholder for that positional tier |

The manual gives example committed values of 1,701, 14, and 3,001 across pendant cords. It also explicitly notes that the complete Andean khipu tradition involves color and other features, and that this introductory encoding does not exhaust the wider computational ecosystem.

The lesson does **not** claim that every historical khipu follows this exact encoding, that the proposed knots are a universal code, or that the archaeological semantics of a specimen can be inferred from a classroom exercise alone. It offers a discoverable modern baseline for moving from a dynamic board state to a durable record.

## 9. Assessment rubric

| Skill | Novice | Proficient | Master |
|---|---|---|---|
| Digit encoding | More than three counters or incorrect values | Encodes 0–9 correctly | Sets a four-digit number fluently and economically |
| Addition and clock step | Misses fusions or carries | Resolves fusions and avalanches | Handles multi-row avalanches without prompting |
| Subtraction and unweaving | Removes from empty cups | Unweaves correctly | Performs multi-tier unweaving fluently |
| Ayni division | Loses scale or allotments | Executes top-down harvesting | Explains the fair-share model while dividing |
| Database commit | Confuses knots and places | Translates a settled state accurately | Explains how the record preserves the board state |

## 10. Student worksheets

Use a physical board and record intermediate states. Suggested problems from the manual:

1. **Addition:** 247 + 385 = 632.
2. **Subtraction:** 1,204 − 531 = 673.
3. **Multiplication:** 64 × 23 = 1,472.
4. **Ayni division:** 3,600 ÷ 24 = 150.

For each exercise, the student should show the initial placement, every unweaving or fusion, every avalanche, and the final settled board. The record is part of the lesson: the learner is not merely asked for an answer but is asked to make the path visible.

## Provenance and limits

- **Source:** supplied PDF, *Educator's Field Manual: The Inka Khipu Arcade & Somatic Compute System*, English edition, 12 pages, 2026.
- **Preserved:** the manual's board topology, cup values, Golden Rule, clock-step operations, unweaving, loom multiplication, Ayni division, proposed introductory knot metrics, assessment rubric, and worksheets.
- **Observed:** the source document explicitly identifies itself as a Basin Game Studios / Mage's Guild Psychonautics educational work and MIT-licensed material.
- **Interpreted:** “ALU / RAM,” “non-volatile software storage,” “clock-step execution,” “gravitational attractor,” and “database commit” are modern computational teaching metaphors and design choices in this manual.
- **Open:** the historical scope of any particular Yupana configuration, the semantics of nonnumeric khipu features, the relationship between this classroom encoding and individual archaeological specimens, and the full diversity of Andean recording practices.

The manual's strongest invitation is practical: put counters on a board, let the state become visible, and let the learner discover that arithmetic can be touched. Its claims become more trustworthy when the line between historical evidence and modern reconstruction stays visible.
