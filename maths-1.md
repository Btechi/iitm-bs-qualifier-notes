# IITM BS Qualifier: Maths I notes (weeks 1–4)

Sets, Venn counting, relations, functions, straight lines, quadratics and polynomial graphs. Every formula and repeat pattern from weeks 1–4.

Read it online, print it or save it as a PDF: **[Maths I cheat sheet on BTechi](https://www.btechi.in/qualifier/notes/maths-1)**. Then test yourself with a [free Maths I qualifier mock test](https://www.btechi.in/qualifier).

## Contents

- [Week 1: Number systems & sets](#sets)
- [Week 1: Venn diagrams & counting](#venn)
- [Week 1: Relations](#relations)
- [Week 1: Functions](#functions)
- [Week 2: Coordinate geometry](#coordinates)
- [Week 2: Straight lines](#lines)
- [Week 2: Straight-line fit](#line-fit)
- [Week 3: Quadratic functions & parabolas](#quadratic-functions)
- [Week 3: Quadratic equations & roots](#quadratic-equations)
- [Week 4: Polynomials: algebra & division](#polynomial-algebra)
- [Week 4: Graphs of polynomials](#polynomial-graphs)
- [Last-minute checklist](#last-minute)

<a id="sets"></a>

## Week 1: Number systems & sets

*asked often in past qualifier papers*

**Number systems**

| | Formula | Note |
|---|---|---|
| Chain | ℕ ⊂ ℤ ⊂ ℚ ⊂ ℝ | IITM lectures take ℕ = {0, 1, 2, …}. Some questions start at 1, so read the definition given. |
| Rational | p/q, p, q ∈ ℤ, q ≠ 0 | Decimal expansion terminates or recurs. |
| Irrational | √2, √3, π, e | Non-terminating, non-recurring. √n is irrational unless n is a perfect square. |
| gcd × lcm | gcd(a, b) × lcm(a, b) = a × b |  |
| From prime factors | gcd = lowest powers of common primes · lcm = highest powers of all primes |  |

**Sets (|A| = n)**

| | Formula | Note |
|---|---|---|
| Power set | \|P(A)\| = 2<sup>n</sup> |  |
| Proper subsets | 2<sup>n</sup> − 1 | Non-empty proper subsets: 2<sup>n</sup> − 2 |
| Subsets of size k | C(n, k) = n!/(k!(n − k)!) |  |
| Cartesian product | \|A × B\| = \|A\| · \|B\| | A × B ≠ B × A unless A = B or one of them is empty. |
| Difference | A \ B = A ∩ B<sup>c</sup>,  \|A \ B\| = \|A\| − \|A ∩ B\| |  |
| De Morgan | (A ∪ B)<sup>c</sup> = A<sup>c</sup> ∩ B<sup>c</sup> · (A ∩ B)<sup>c</sup> = A<sup>c</sup> ∪ B<sup>c</sup> |  |

*Diagram: Number systems, nested.* Every natural number is an integer, every integer is rational, and the rationals plus the irrationals make up ℝ. [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#sets).

- ∅ is a subset of every set, and every set is a subset of itself.
- {∅} is **not** empty: it has one element.
- Repeats and order don't matter: {1, 2, 2} = {2, 1}.
- Set-builder: list it out before counting. {x ∈ ℤ | −2 < x ≤ 3} = {−1, 0, 1, 2, 3}.
- Intervals: [a, b] includes both ends, (a, b) excludes them.

> [!WARNING]
> **Common traps**
> - ∈ is for elements, ⊆ is for sets: 1 ∈ {1, 2} but {1} ⊆ {1, 2}.
> - 0 is an integer and a rational number (0/1). It is neither positive nor negative.
> - 22/7 and 1.414 are rational; π and √2 are not.

<a id="venn"></a>

## Week 1: Venn diagrams & counting

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Two sets | \|A ∪ B\| = \|A\| + \|B\| − \|A ∩ B\| |  |
| Three sets | \|A ∪ B ∪ C\| = \|A\| + \|B\| + \|C\| − \|A ∩ B\| − \|B ∩ C\| − \|A ∩ C\| + \|A ∩ B ∩ C\| |  |
| Only A | \|A\| − \|A ∩ B\| − \|A ∩ C\| + \|A ∩ B ∩ C\| |  |
| A and B, not C | \|A ∩ B\| − \|A ∩ B ∩ C\| |  |
| Exactly two | (\|A ∩ B\| + \|B ∩ C\| + \|A ∩ C\|) − 3\|A ∩ B ∩ C\| |  |
| Exactly one | \|A\| + \|B\| + \|C\| − 2(\|A ∩ B\| + \|B ∩ C\| + \|A ∩ C\|) + 3\|A ∩ B ∩ C\| |  |
| Neither / none | Total − \|A ∪ B ∪ C\| |  |
| Largest overlap | \|A ∩ B\|<sub>max</sub> = min(\|A\|, \|B\|) |  |
| Smallest overlap | \|A ∩ B\|<sub>min</sub> = max(0, \|A\| + \|B\| − Total) |  |

> [!TIP]
> Fill the diagram **from the centre outwards**: the triple overlap first, then the 'exactly two' regions, then the 'only' regions, then 'none' outside. Every sub-question is then just adding regions.

*Diagram: The Jan 2024 PYQ, filled in.* Start with the 5 in the centre. Take it off each pair (20 − 5, 15 − 5, 10 − 5), then fill the singles. The union is 80, so 20 bought none. [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#venn).

**Example: PYQ pattern (Sep 2023)**

In a group of 60 people, 40 like cricket and 35 like football. (a) What is the minimum number who like both? (b) If 10 like neither, how many like only cricket?

1. (a) Both ≥ 40 + 35 − 60 = 15.
2. (b) At least one = 60 − 10 = 50, so both = 40 + 35 − 50 = 25.
3. Only cricket = 40 − 25 = 15.

**Answer:** (a) 15 · (b) 15

**Example: PYQ pattern (Jan 2024)**

Of 100 customers, 50 bought milk, 40 bread and 30 fruits. 20 bought milk and bread, 15 milk and fruits, 10 bread and fruits, and 5 bought all three. How many bought milk and fruits but not bread? How many bought none?

1. Milk and fruits, not bread = 15 − 5 = 10.
2. Union = 50 + 40 + 30 − 20 − 15 − 10 + 5 = 80.
3. None = 100 − 80 = 20.

**Answer:** 10 and 20

> [!WARNING]
> **Common traps**
> - 'Both A and B' includes people who are also in C. 'Only A and B' does not.
> - 'At least one' is the union. 'Neither' is total − union.
> - If the total isn't given, never assume 'none' is 0.

<a id="relations"></a>

## Week 1: Relations

*asked in every paper in past qualifier papers*

**Definitions (|A| = n)**

| | Formula | Note |
|---|---|---|
| Relation on A | R ⊆ A × A |  |
| Number of relations | 2<sup>n²</sup> |  |
| Reflexive | (a, a) ∈ R for **every** a ∈ A | Number of reflexive relations: 2<sup>n² − n</sup> |
| Symmetric | (a, b) ∈ R ⇒ (b, a) ∈ R | Number of symmetric relations: 2<sup>n(n + 1)/2</sup> |
| Antisymmetric | (a, b) ∈ R and (b, a) ∈ R ⇒ a = b |  |
| Transitive | (a, b) ∈ R and (b, c) ∈ R ⇒ (a, c) ∈ R |  |
| Equivalence | reflexive + symmetric + transitive |  |
| Pairs not in R | \|(A × A) \ R\| = n² − \|R\| |  |

*Diagram: The four properties as arrow diagrams.* An arrow a → b means (a, b) ∈ R. A loop on a node is (a, a). [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#relations).

**Standard relations**

| Relation | Refl. | Sym. | Anti. | Trans. |
|---|---|---|---|---|
| Identity {(a, a)} | ✓ | ✓ | ✓ | ✓ |
| Empty ∅ (A non-empty) | ✗ | ✓ | ✓ | ✓ |
| Universal A × A (\|A\| ≥ 2) | ✓ | ✓ | ✗ | ✓ |
| a ≤ b | ✓ | ✗ | ✓ | ✓ |
| a < b | ✗ | ✗ | ✓ | ✓ |
| a divides b (positive integers) | ✓ | ✗ | ✓ | ✓ |
| a − b is even (integers) | ✓ | ✓ | ✗ | ✓ |
| a ≠ b | ✗ | ✓ | ✗ | ✗ |
| Line ⊥ line | ✗ | ✓ | ✗ | ✗ |

**Example: PYQ (May 2023)**

The Cartesian product A × A has 9 elements. Two of them are (2, 0) and (0, 8). Find the sum of all the elements of A.

1. |A|² = 9, so |A| = 3.
2. (2, 0) and (0, 8) put 2, 0 and 8 in A, so A = {0, 2, 8}.
3. Sum = 0 + 2 + 8.

**Answer:** 10

**Example**

S = {1, 2, 3, 4} and R = {(a, b) ∈ S × S : a divides b}. Find |R| and |(S × S) \ R|.

1. a = 1: b = 1, 2, 3, 4 → 4 pairs.
2. a = 2: b = 2, 4 → 2 pairs. a = 3: (3, 3). a = 4: (4, 4).
3. |R| = 8, and |S × S| = 16, so 16 − 8 = 8 pairs are not in R.

**Answer:** |R| = 8 · |(S × S) \ R| = 8

> [!TIP]
> Write R out as a list of pairs first (it's usually under 15 pairs), then test each property against that list. Reasoning from the rule alone is where marks are lost.

> [!WARNING]
> **Common traps**
> - **Transitivity trap:** if (1, 2) and (2, 1) are in R, then (1, 1) **and** (2, 2) must be in R too.
> - Reflexive needs (a, a) for every element of A, including elements that never appear in R.
> - Symmetric and antisymmetric aren't opposites. The identity relation is both; {(1, 2), (2, 1), (1, 3)} is neither.
> - No chain (a, b), (b, c) at all? Then R is transitive (vacuously). ∅ is symmetric and transitive.

<a id="functions"></a>

## Week 1: Functions

*asked often in past qualifier papers*

**|A| = m, |B| = n**

| | Formula | Note |
|---|---|---|
| Function f: A → B | every a ∈ A has **exactly one** image in B |  |
| Range | {f(a) : a ∈ A} ⊆ codomain B |  |
| One-one (injective) | f(a<sub>1</sub>) = f(a<sub>2</sub>) ⇒ a<sub>1</sub> = a<sub>2</sub> |  |
| Onto (surjective) | range = codomain |  |
| Bijective | one-one + onto ⇒ f<sup>−1</sup> exists |  |
| Functions A → B | n<sup>m</sup> |  |
| One-one functions (m ≤ n) | n!/((n − m)!) |  |
| Bijections (m = n) | n! |  |
| Composition | (g ∘ f)(x) = g(f(x)) | Usually g ∘ f ≠ f ∘ g. |

*Diagram: Mapping diagrams.* [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#functions).

**Tests and domains**

| Check | Rule |
|---|---|
| Vertical line test | Every vertical line meets the graph at most once ⇒ it is a function |
| Horizontal line test | Every horizontal line meets the graph at most once ⇒ one-one |
| √(g(x)) | Domain: g(x) ≥ 0 |
| 1/(g(x)) | Domain: g(x) ≠ 0 |
| log g(x) | Domain: g(x) > 0 |

**Standard functions, ℝ → ℝ**

| f(x) | One-one? | Onto? |
|---|---|---|
| ax + b (a ≠ 0) | ✓ | ✓ |
| x² | ✗ | ✗ (range [0, ∞)) |
| x³ | ✓ | ✓ |
| \|x\| | ✗ | ✗ |
| e<sup>x</sup> | ✓ | ✗ (range (0, ∞)) |
| x² on [0, ∞) → [0, ∞) | ✓ | ✓ |

> [!WARNING]
> **Common traps**
> - Changing the domain or codomain changes the answer: x² is not one-one on ℝ, but is on [0, ∞).
> - If some element of A has no image, or two images, it is not a function at all.
> - Onto depends on the codomain the question states, not on the formula.

<a id="coordinates"></a>

## Week 2: Coordinate geometry

*asked often in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Distance | d = √((x<sub>2</sub> − x<sub>1</sub>)² + (y<sub>2</sub> − y<sub>1</sub>)²) |  |
| Midpoint | ((x<sub>1</sub> + x<sub>2</sub>)/2, (y<sub>1</sub> + y<sub>2</sub>)/2) |  |
| Section, internal m : n | ((mx<sub>2</sub> + nx<sub>1</sub>)/(m + n), (my<sub>2</sub> + ny<sub>1</sub>)/(m + n)) |  |
| Section, external m : n | ((mx<sub>2</sub> − nx<sub>1</sub>)/(m − n), (my<sub>2</sub> − ny<sub>1</sub>)/(m − n)) |  |
| Centroid | ((x<sub>1</sub> + x<sub>2</sub> + x<sub>3</sub>)/3, (y<sub>1</sub> + y<sub>2</sub> + y<sub>3</sub>)/3) |  |
| Area of triangle | ½ \|x<sub>1</sub>(y<sub>2</sub> − y<sub>3</sub>) + x<sub>2</sub>(y<sub>3</sub> − y<sub>1</sub>) + x<sub>3</sub>(y<sub>1</sub> − y<sub>2</sub>)\| |  |
| Collinear points | area = 0 (or equal slopes) |  |
| Distance from the axes | from x-axis: \|y\| · from y-axis: \|x\| |  |

**Reflections and quadrants**

| Reflect (x, y) in | Result |
|---|---|
| x-axis | (x, −y) |
| y-axis | (−x, y) |
| Origin | (−x, −y) |
| Line y = x | (y, x) |
| Quadrant signs | I (+, +) · II (−, +) · III (−, −) · IV (+, −) |

*Diagram: Quadrants and reflections of P(3, 1).* [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#coordinates).

**Example: PYQ pattern (Jan 2023)**

Starting at the origin, Ajay walks 3 units right, 4 units up, then 6 units left. Where is he, and how far is he from home?

1. (0, 0) → (3, 0) → (3, 4) → (−3, 4).
2. Distance = √((−3)² + 4²) = √25.

**Answer:** (−3, 4) in quadrant II, 5 units from home

> [!WARNING]
> **Common traps**
> - In the section formula, m multiplies the **second** point (x<sub>2</sub>, y<sub>2</sub>).
> - Area can't be negative: take the absolute value.

<a id="lines"></a>

## Week 2: Straight lines

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Slope from 2 points | m = (y<sub>2</sub> − y<sub>1</sub>)/(x<sub>2</sub> − x<sub>1</sub>) = tan θ |  |
| Point–slope | y − y<sub>1</sub> = m(x − x<sub>1</sub>) |  |
| Slope–intercept | y = mx + c |  |
| Intercept form | x/a + y/b = 1 | x-intercept a, y-intercept b |
| General form | ax + by + c = 0 ⇒ slope −a/b, x-int −c/a, y-int −c/b |  |
| Horizontal / vertical | y = k (slope 0) · x = k (slope undefined) |  |
| Parallel | m<sub>1</sub> = m<sub>2</sub> | Line parallel to ax + by + c = 0: ax + by + k = 0 |
| Perpendicular | m<sub>1</sub>m<sub>2</sub> = −1 | Line perpendicular to ax + by + c = 0: bx − ay + k = 0 |
| Angle between lines | tan θ = \|(m<sub>1</sub> − m<sub>2</sub>)/(1 + m<sub>1</sub>m<sub>2</sub>)\| |  |
| Point to line | d = (\|ax<sub>1</sub> + by<sub>1</sub> + c\|)/(√(a² + b²)) |  |
| Between parallel lines | d = (\|c<sub>1</sub> − c<sub>2</sub>\|)/(√(a² + b²)) |  |
| Foot of perpendicular | (x − x<sub>1</sub>)/a = (y − y<sub>1</sub>)/b = −(ax<sub>1</sub> + by<sub>1</sub> + c)/(a² + b²) |  |

*Diagram: Lines at a glance.* [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#lines).

**Example: PYQ (May 2024)**

L₁ passes through P₁(3, −2) and has x-intercept 1. L₂ passes through P₂(−1, 5) and has y-intercept −1. If θ is the angle between them, find tan θ.

1. L₁ passes through (1, 0) and (3, −2): m<sub>1</sub> = (−2 − 0)/(3 − 1) = −1.
2. L₂ passes through (0, −1) and (−1, 5): m<sub>2</sub> = (5 − (−1))/(−1 − 0) = −6.
3. tan θ = |(−1 − (−6))/(1 + (−1)(−6))| = 5/7.

**Answer:** tan θ = 5/7

**Example**

Where do 2x + y = 7 and x − y = −1 meet?

1. Add the equations: 3x = 6, so x = 2.
2. Then y = 7 − 2(2) = 3.

**Answer:** (2, 3)

> [!WARNING]
> **Common traps**
> - Slope of ax + by + c = 0 is **−a/b**. Not a/b, not −b/a.
> - Intercept form needs 1 on the right: 3x + 4y = 12 → x/4 + y/3 = 1.
> - 1 + m<sub>1</sub>m<sub>2</sub> = 0 means the lines are perpendicular (θ = 90°), so tan θ is undefined.
> - Before using the parallel-line distance, make the x and y coefficients identical: x + 2y − 3 = 0 becomes 2x + 4y − 6 = 0 to compare with 2x + 4y + 1 = 0.

<a id="line-fit"></a>

## Week 2: Straight-line fit

*asked sometimes in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Error (residual) | e<sub>i</sub> = y<sub>i</sub> − ŷ<sub>i</sub> | actual − predicted |
| Sum of squared errors | SSE = Σ (y<sub>i</sub> − ŷ<sub>i</sub>)² |  |
| Better fit | the line with the **smaller** SSE |  |
| Least-squares line | m = (nΣxy − ΣxΣy)/(nΣx² − (Σx)²),  c = y̅ − mx̅ |  |

*Diagram: Errors are vertical gaps.* SSE adds up the squared red gaps. The least-squares line makes that total as small as possible. [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#line-fit).

**Example**

Points (1, 2), (2, 3), (3, 5). Which fits better: y = x + 1 or y = 1.5x + 0.5?

1. y = x + 1 predicts 2, 3, 4 → errors 0, 0, 1 → SSE = 1.
2. y = 1.5x + 0.5 predicts 2, 3.5, 5 → errors 0, −0.5, 0 → SSE = 0.25.

**Answer:** y = 1.5x + 0.5 (SSE 0.25 < 1)

> [!TIP]
> The least-squares line always passes through (x̅, y̅). Use it to knock out options without computing m.

<a id="quadratic-functions"></a>

## Week 3: Quadratic functions & parabolas

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Standard form | f(x) = ax² + bx + c, a ≠ 0 |  |
| Vertex x | h = −b/2a |  |
| Vertex y | k = f(h) = −D/4a = c − b²/4a |  |
| Axis of symmetry | x = −b/2a |  |
| Vertex form | f(x) = a(x − h)² + k |  |
| Opens | a > 0: up, minimum = k · a < 0: down, maximum = k |  |
| Range | a > 0: [k, ∞) · a < 0: (−∞, k] |  |
| y-intercept | (0, c) |  |
| Slope at x (tangent) | 2ax + b | Zero at the vertex. |
| Slope of secant x₁ → x₂ | (f(x<sub>2</sub>) − f(x<sub>1</sub>))/(x<sub>2</sub> − x<sub>1</sub>) = a(x<sub>1</sub> + x<sub>2</sub>) + b |  |
| Increasing / decreasing | a > 0: decreasing on (−∞, h), increasing on (h, ∞) | Reversed when a < 0. |

*Diagram: Reading a parabola.* [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#quadratic-functions).

**Example: PYQ (May 2024)**

y = x² + 4x + 12. Find the vertex, the minimum value, the x-intercepts and the range.

1. a = 1 > 0, so it opens up.
2. h = −4/2 = −2, k = 4 − 8 + 12 = 8 → vertex (−2, 8).
3. D = 16 − 48 = −32 < 0 → no x-intercepts. y-intercept = 12.

**Answer:** Vertex (−2, 8), minimum 8, no x-intercepts, range [8, ∞)

**Example: PYQ pattern (May 2023)**

Profit P(x) = −2x² + 24x − 40, where x is tonnes of raw material. For what x is profit maximum, and when is profit zero?

1. x = −24/(2(−2)) = 6, and P(6) = −72 + 144 − 40 = 32.
2. P(x) = 0 ⇒ x² − 12x + 20 = 0 ⇒ (x − 2)(x − 10) = 0.

**Answer:** Maximum profit 32 at x = 6; zero profit at x = 2 and x = 10

> [!WARNING]
> **Common traps**
> - The max/min **value** is k (the y-coordinate). The input that gives it is h. Read which one is asked.
> - Vertex x is −b/(2a): keep both the minus sign and the 2.
> - D < 0 with a > 0 means the parabola is entirely above the x-axis, so f(x) > 0 for every x.

<a id="quadratic-equations"></a>

## Week 3: Quadratic equations & roots

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Roots | x = (−b ± √D)/2a,  D = b² − 4ac |  |
| Nature of roots | D > 0: two distinct real · D = 0: equal, x = −b/2a · D < 0: no real roots |  |
| Rational roots | D is a perfect square (a, b, c rational) |  |
| Sum and product | α + β = −b/a,  αβ = c/a |  |
| Equation from roots | x² − (α + β)x + αβ = 0 |  |
| Sum of squares | α² + β² = (α + β)² − 2αβ |  |
| Difference | \|α − β\| = √D/(\|a\|) |  |
| Reciprocals | 1/(α) + 1/(β) = (α + β)/(αβ) |  |
| Cubes | α³ + β³ = (α + β)³ − 3αβ(α + β) |  |
| Signs of roots | c/a < 0 ⇒ opposite signs · both positive ⇔ −b/a > 0 and c/a > 0 | For real roots (D ≥ 0). |
| Completing the square | ax² + bx + c = a(x + b/2a)² − D/4a |  |

*Diagram: The discriminant decides the picture.* [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#quadratic-equations).

**Example: PYQ pattern (Jan 2024)**

Ram copied the constant term wrongly and got roots 3 and 4. Shyam copied the x-coefficient wrongly and got roots 1 and 10. Find the correct roots.

1. Ram's mistake doesn't touch b, so the sum is right: α + β = 7.
2. Shyam's mistake doesn't touch c, so the product is right: αβ = 10.
3. x² − 7x + 10 = 0 ⇒ (x − 2)(x − 5) = 0.

**Answer:** 2 and 5

**Example**

For which k does x² − kx + 9 = 0 have equal roots?

1. Equal roots ⇒ D = 0.
2. k² − 36 = 0.

**Answer:** k = ±6

> [!TIP]
> Roots given and the equation asked? Don't expand anything. Check each option's −b/a and c/a against the sum and product.

> [!WARNING]
> **Common traps**
> - Wrong constant ⇒ the **sum** is still right. Wrong x-coefficient ⇒ the **product** is still right.
> - x-intercepts of the graph are the real roots. D < 0 ⇒ the graph never meets the x-axis.

<a id="polynomial-algebra"></a>

## Week 4: Polynomials: algebra & division

*asked often in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Degree | highest power with a non-zero coefficient |  |
| Degree rules | deg(pq) = deg p + deg q · deg(p ± q) ≤ max(deg p, deg q) |  |
| Division algorithm | p(x) = d(x) · q(x) + r(x),  deg r < deg d |  |
| Remainder theorem | p(x) ÷ (x − a) leaves remainder p(a) | ÷ (ax − b) leaves p(b/a) |
| Factor theorem | (x − a) is a factor ⇔ p(a) = 0 |  |
| Sum of coefficients | p(1) | Alternating sum: p(−1) |
| Rational root test | possible roots = ±(factors of constant)/(factors of leading coefficient) |  |
| Cubic ax³ + bx² + cx + d | α + β + γ = −b/a,  αβ + βγ + γα = c/a,  αβγ = −d/a |  |

**Identities**

| | Formula | Note |
|---|---|---|
| Square | (a ± b)² = a² ± 2ab + b² |  |
| Difference of squares | a² − b² = (a + b)(a − b) |  |
| Cube | (a + b)³ = a³ + b³ + 3ab(a + b) |  |
| Sum / difference of cubes | a³ ± b³ = (a ± b)(a² ∓ ab + b²) |  |

*Diagram: Remainder and factor theorem.* x³ − 2x² + 4x − 5 divided by (x − 2): p(2) = 3, which isn't 0, so the remainder is 3. [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#polynomial-algebra).

**Example**

Find the remainder when p(x) = x³ − 2x² + 4x − 5 is divided by (x − 2).

1. Remainder = p(2) = 8 − 8 + 8 − 5.

**Answer:** 3

**Example**

(x − 1) is a factor of x³ + kx² − 4x + 2. Find k.

1. p(1) = 0 ⇒ 1 + k − 4 + 2 = 0.

**Answer:** k = 1

<a id="polynomial-graphs"></a>

## Week 4: Graphs of polynomials

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Real roots | degree n ⇒ at most n x-intercepts |  |
| Turning points | at most n − 1 |  |
| Odd degree | at least 1 real root; the two ends point opposite ways |  |
| Even degree | both ends point the same way; may have no real root |  |
| Factor form | p(x) = a(x − r<sub>1</sub>)<sup>k₁</sup>(x − r<sub>2</sub>)<sup>k₂</sup>⋯,  degree = k<sub>1</sub> + k<sub>2</sub> + ⋯ |  |
| y-intercept | p(0) |  |

*Diagram: End behaviour.* [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#polynomial-graphs).

**End behaviour (leading term aₙxⁿ)**

|  | aₙ > 0 | aₙ < 0 |
|---|---|---|
| n even | ↑ … ↑ (both ends up) | ↓ … ↓ (both ends down) |
| n odd | ↓ … ↑ (down-left, up-right) | ↑ … ↓ (up-left, down-right) |

**Multiplicity at a root r**

| Factor | At x = r the graph |
|---|---|
| (x − r)¹ | crosses straight through |
| (x − r)², any even power | touches the axis and bounces back (no sign change) |
| (x − r)³, odd power ≥ 3 | crosses but flattens out (S-shape) |

- Reading a graph: a crossing root has odd multiplicity; a touching root has even multiplicity (usually 2).
- Minimum degree from a graph = sum of the multiplicities you can see, and at least (turning points + 1).
- Find the leading coefficient a by substituting the y-intercept or any labelled point.
- p(x) changes sign only at odd-multiplicity roots. Use a sign chart for 'p(x) > 0 when?' questions.

**Example**

Describe the graph of p(x) = (x + 2)(x − 1)².

1. Degree 3 with positive leading coefficient: starts down-left, ends up-right.
2. x = −2 (power 1): crosses. x = 1 (power 2): touches and bounces.
3. y-intercept p(0) = 2 × 1 = 2. Two turning points.
4. Sign: negative for x < −2, positive between −2 and 1, positive for x > 1.

**Answer:** Crosses at −2, bounces at 1, y-intercept 2

*Diagram: The worked example, drawn.* [View it on BTechi](https://www.btechi.in/qualifier/notes/maths-1#polynomial-graphs).

**Example: PYQ pattern (every paper has a graph)**

A degree-4 polynomial crosses the x-axis at −1 and 3, touches it at 1, and p(0) = 6. Find p(x).

1. p(x) = a(x + 1)(x − 3)(x − 1)²: degree 1 + 1 + 2 = 4 ✓.
2. p(0) = a(1)(−3)(1) = −3a = 6 ⇒ a = −2.
3. Leading coefficient negative ⇒ both ends point down.

**Answer:** p(x) = −2(x + 1)(x − 3)(x − 1)²

> [!WARNING]
> **Common traps**
> - 'Distinct roots' counts each root once. Counted with multiplicity, (x − 1)² is two roots.
> - Turning points aren't roots: x³ has 1 root and 0 turning points; (x + 2)(x − 1)² has 2 distinct roots and 2 turning points.
> - At an even-multiplicity root the graph does **not** change sign.

<a id="last-minute"></a>

## Last-minute checklist

- [ ] |A ∪ B ∪ C| = Σ|A| − Σ|A ∩ B| + |A ∩ B ∩ C|. Fill Venn diagrams from the centre out.
- [ ] Transitive trap: (a, b) and (b, a) in R ⇒ (a, a) and (b, b) must be in R.
- [ ] |P(A)| = 2<sup>n</sup>, relations on A: 2<sup>n²</sup>, functions A → B: |B|<sup>|A|</sup>.
- [ ] Slope of ax + by + c = 0 is −a/b. Perpendicular ⇔ m<sub>1</sub>m<sub>2</sub> = −1.
- [ ] tan θ = |(m<sub>1</sub> − m<sub>2</sub>) / (1 + m<sub>1</sub>m<sub>2</sub>)|.
- [ ] Point to line: |ax<sub>1</sub> + by<sub>1</sub> + c| / √(a² + b²).
- [ ] Vertex at x = −b/2a, extreme value −D/4a.
- [ ] α + β = −b/a, αβ = c/a. Wrong constant keeps the sum; wrong x-coefficient keeps the product.
- [ ] Odd multiplicity crosses, even multiplicity touches.
- [ ] Degree n ⇒ at most n roots and at most n − 1 turning points.

---

From [BTechi](https://www.btechi.in), a free, independent study site for the IIT Madras BS. Not affiliated with IIT Madras. Found a mistake? [Open an issue](https://github.com/Btechi/iitm-bs-qualifier-notes/issues) or use the Report button on the [online sheet](https://www.btechi.in/qualifier/notes/maths-1).
