# IITM BS Qualifier: Stats I notes (weeks 1–4)

Data types and scales, charts, mean/median/mode, variance, IITM's percentile method, outliers, contingency tables, covariance, correlation and point bi-serial.

Read it online, print it or save it as a PDF: **[Stats I cheat sheet on BTechi](https://www.btechi.in/qualifier/notes/stats-1)**. Then test yourself with a [free Stats I qualifier mock test](https://www.btechi.in/qualifier).

## Contents

- [Week 1: Data, population & sample](#data-basics)
- [Week 1: Variable types & scales of measurement](#scales)
- [Week 2: Describing categorical data](#categorical-data)
- [Week 3: Numerical data: tables & charts](#numerical-displays)
- [Week 3: Mean, median & mode](#central-tendency)
- [Week 3: Range, variance & standard deviation](#dispersion)
- [Week 3: Percentiles, quartiles, IQR & outliers](#percentiles)
- [Week 4: Two categorical variables](#two-categorical)
- [Week 4: Scatter plots & covariance](#covariance)
- [Week 4: Correlation coefficient (r)](#correlation)
- [Week 4: Point bi-serial correlation](#point-biserial)
- [Last-minute checklist](#last-minute)

<a id="data-basics"></a>

## Week 1: Data, population & sample

*asked in every paper in past qualifier papers*

| Term | Meaning |
|---|---|
| Population | The entire group you want to study (all voters in India) |
| Sample | The subset you actually collect data from |
| Parameter | A number describing the population (μ, σ) |
| Statistic | A number computed from a sample (x̅, s) |
| Descriptive statistics | Organising and summarising data: tables, charts, mean, SD |
| Inferential statistics | Using a sample to draw conclusions about the population |
| Cross-sectional data | Many units at **one** point in time (marks of 500 students in one exam) |
| Time-series data | One unit tracked **over time** (a company's yearly profit, 2015–2024) |
| Case / observation | A row of the data table (one unit) |
| Variable | A column: a characteristic recorded for every case |

*Diagram: Population, sample and inference.* [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#data-basics).

- For inference to be valid, the sample must be **representative** of the population: randomly chosen and unbiased.
- A claim about every organisation in a city based on one organisation's data is an over-generalisation: the sample doesn't represent the population.

*Diagram: Cross-sectional vs time series.* [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#data-basics).

> [!WARNING]
> **Common traps**
> - Data from many villages or students collected at one time is cross-sectional, even if the table has a 'year' column.
> - Survey 100 students to learn about all IITM students: population = all IITM students, sample = the 100.

<a id="scales"></a>

## Week 1: Variable types & scales of measurement

*asked in every paper in past qualifier papers*

**Categorical vs numerical**

| Type | What it is | Examples |
|---|---|---|
| Categorical (qualitative) | Labels or groups | Gender, city, blood group, T-shirt size, PIN code, roll number |
| Numerical, discrete | Countable values with gaps | Children in a family, cars sold, goals scored |
| Numerical, continuous | Any value in a range (measured) | Height, weight, time, temperature |

**Scales: N-O-I-R, each adds one property**

| Scale | Adds | Allowed | Examples | Centre |
|---|---|---|---|---|
| Nominal | Names only, no order | = ≠ | Gender, religion, election symbol, city, jersey number | Mode |
| Ordinal | Order (gaps unequal) | < > | Ratings, ranks, grades, sizes S/M/L/XL, education level | Mode, median |
| Interval | Equal gaps, **no true zero** | + − | Temperature in °C/°F, calendar year, time of day | Mode, median, mean |
| Ratio | True zero (0 = none) | + − × ÷ | Height, weight, income, age, sales, number of votes | All |

> [!TIP]
> Ask in order: Is it just a label? → nominal. Can I put it in order? → ordinal. Does 0 mean 'none of it'? → ratio; if not → interval.

*Diagram: Which scale? Ask in order.* [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#scales).

> [!WARNING]
> **Common traps**
> - Numbers used as labels (PIN code, roll number, phone number, jersey number) are **categorical, nominal**.
> - °C is interval: 0 °C isn't 'no temperature', and 20 °C isn't twice as hot as 10 °C.
> - Counts (votes, children, cars) are numerical, discrete, ratio scale.
> - PYQ (May 2024): election symbol is categorical with a nominal scale.

<a id="categorical-data"></a>

## Week 2: Describing categorical data

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Relative frequency | f/n | All relative frequencies add to 1. |
| Percentage | f/n × 100 |  |
| Pie-chart angle | f/n × 360° |  |
| Count from a slice | n × angle/(360°)  or  n × percentage |  |
| Mode | the category with the highest frequency |  |
| Median (ordinal only) | the middle category after ordering |  |

**Charts**

| Chart | Rule |
|---|---|
| Bar chart | One bar per category, gaps between bars, height = frequency |
| Pie chart | Parts of a whole; slices add to 100% (360°) |
| Pareto chart | Bars in **descending** order plus a cumulative-percentage line |
| Stacked / side-by-side bars | Two categorical variables together (week 4) |

*Diagram: Pie and Pareto charts of 500 fruits.* [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#categorical-data).

**Example: PYQ pattern (Sep 2023)**

A pie chart of 500 fruits sold shows mangoes as a 72° slice. How many mangoes were sold?

1. 72/360 × 500

**Answer:** 100

**Example: PYQ pattern (Sep 2023)**

Sunidhi buys T-shirts of sizes M, L, S, XL, S, then one more M. What happens to the mode and the median?

1. Before: S, S, M, L, XL → mode S, median (3rd) M.
2. After: S, S, M, M, L, XL → S and M both appear twice: bimodal.
3. Median = 3rd and 4th = M and M → M.

**Answer:** Mode becomes S and M; median stays M

> [!WARNING]
> **Common traps**
> - Mean makes no sense for categorical data, even when categories are coded as numbers.
> - Median needs order: fine for ordinal, meaningless for nominal.
> - Data can have more than one mode.
> - Misleading graphs: y-axis not starting at 0, 3-D pies, bars of unequal width.

<a id="numerical-displays"></a>

## Week 3: Numerical data: tables & charts

*asked often in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Class width | upper limit − lower limit |  |
| Class mark (midpoint) | (lower + upper)/2 |  |
| Mean of grouped data | (Σ f<sub>i</sub>x<sub>i</sub>)/(Σ f<sub>i</sub>) | x<sub>i</sub> = class midpoint |

- Class [10, 20) includes 10 and excludes 20; a value of exactly 20 goes in the next class.
- Histogram: bars touch (no gaps); bar area ∝ frequency. Bar charts are for categories, histograms for numbers.
- Stem-and-leaf: stem 2 | leaf 3 means 23. Number of leaves = n. You keep every actual value, so counts, median and mean can be read straight off.
- Shape: symmetric (mean ≈ median); right-skewed, long tail to the right (mean > median); left-skewed (mean < median).

*Diagram: Shape tells you where the mean sits.* The mean is dragged towards the long tail; the median stays with the bulk of the data. [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#numerical-displays).

**Example: PYQ pattern (May 2024)**

Ages in a stem-and-leaf plot: 1 | 8 9 · 2 | 0 2 3 5 7 · 3 | 1 4. How many are above 23? What is the median?

1. Values: 18, 19, 20, 22, 23, 25, 27, 31, 34 (n = 9).
2. Above 23: 25, 27, 31, 34.
3. Median = 5th value.

**Answer:** 4 people above 23; median 23

> [!WARNING]
> **Common traps**
> - 'Above 23' excludes 23; 'at least 23' includes it.

<a id="central-tendency"></a>

## Week 3: Mean, median & mode

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Mean | x̅ = (Σ x<sub>i</sub>)/n |  |
| Median (sorted data) | n odd: value at position (n + 1)/2 · n even: average of positions n/2 and n/2 + 1 |  |
| Mode | most frequent value (there may be none, or several) |  |
| Combined mean | (n<sub>1</sub>x̅<sub>1</sub> + n<sub>2</sub>x̅<sub>2</sub>)/(n<sub>1</sub> + n<sub>2</sub>) |  |
| Add one value x | new mean = (nx̅ + x)/(n + 1) |  |
| Fix a wrong value | new mean = x̅ + (correct − wrong)/n |  |
| y = ax + b | y̅ = ax̅ + b | Median, mode, quartiles and percentiles transform the same way. |

*Diagram: One outlier moves the mean, not the median.* [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#central-tendency).

**Example: PYQ pattern (Sep 2023)**

The average annual package is ₹8 lakh. Each value has 5 subtracted from it and is then doubled. What is the new average?

1. y = 2(x − 5) ⇒ y̅ = 2(x̅ − 5) = 2 × 3.

**Answer:** ₹6 lakh

> [!WARNING]
> **Common traps**
> - Sort before finding the median.
> - Outliers pull the mean; the median barely moves. Skewed data ⇒ the median is the better centre.
> - Order matters: 2(x̅ − 5) ≠ 2x̅ − 5.

<a id="dispersion"></a>

## Week 3: Range, variance & standard deviation

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Range | max − min |  |
| Population variance | σ² = (Σ(x<sub>i</sub> − μ)²)/n = (Σ x<sub>i</sub>²)/n − μ² |  |
| Sample variance | s² = (Σ(x<sub>i</sub> − x̅)²)/(n − 1) = (Σ x<sub>i</sub>² − nx̅²)/(n − 1) |  |
| Standard deviation | √variance | Same units as the data. |
| Sample ↔ population | s² = n/(n − 1) σ² |  |
| y = ax + b | Var(y) = a² Var(x),  SD(y) = \|a\| SD(x) |  |
| Recover Σx² | sample: (n − 1)s² + nx̅² · population: n(σ² + μ²) |  |

*Diagram: Adding vs multiplying.* Dashed: the original data. [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#dispersion).

**What changes under y = ax + b**

| Measure | Adding b | Multiplying by a |
|---|---|---|
| Mean, median, mode, quartiles | + b | × a |
| Range, IQR | no change | × \|a\| |
| Variance | no change | × a² |
| Standard deviation | no change | × \|a\| |

**Example: PYQ (May 2023)**

10 observations have mean 22 and sample variance 81. One value, 20, was recorded as 15. Find the correct sample standard deviation.

1. Σx = 10 × 22 = 220 → 220 − 15 + 20 = 225, so the mean is 22.5.
2. Σx² = 9 × 81 + 10 × 22² = 729 + 4840 = 5569 → 5569 − 15² + 20² = 5744.
3. s² = (5744 − 10 × 22.5²)/9 = 681.5/9 = 75.72.
4. s = √75.72.

**Answer:** ≈ 8.70 (the official key accepts 8.68–8.71)

**Example**

Marks have mean 40 and sample variance 25. Each mark has 5 subtracted and is then doubled. New mean, variance and SD?

1. Mean: 2(40 − 5) = 70.
2. Variance: 2² × 25 = 100 (subtracting 5 changes nothing).
3. SD: √100.

**Answer:** Mean 70, variance 100, SD 10

> [!WARNING]
> **Common traps**
> - Sample ⇒ divide by n − 1. Population ⇒ divide by n. Read 'sample' or 'population' in the question.
> - Adding or subtracting a constant never changes variance, SD, range or IQR.
> - Multiplying by −2: variance × 4, SD × 2 (SD is never negative).
> - Round only at the very end; carry at least 4 decimals in between.

<a id="percentiles"></a>

## Week 3: Percentiles, quartiles, IQR & outliers

*asked in every paper in past qualifier papers*

**IITM's percentile method (the answer keys use it)**

| | Formula | Note |
|---|---|---|
| Step 1 | sort the data in ascending order |  |
| Step 2: index | i = P/100 × n |  |
| Step 3 | i not whole ⇒ round **up**, take that value · i whole ⇒ average the values at positions i and i + 1 |  |
| Quartiles | Q<sub>1</sub> = P<sub>25</sub>,  Q<sub>2</sub> = P<sub>50</sub> = median,  Q<sub>3</sub> = P<sub>75</sub> |  |
| IQR | Q<sub>3</sub> − Q<sub>1</sub> |  |
| Five-number summary | min, Q<sub>1</sub>, median, Q<sub>3</sub>, max | This is what a box plot draws. |
| Outliers | below Q<sub>1</sub> − 1.5 × IQR  or  above Q<sub>3</sub> + 1.5 × IQR |  |

*Diagram: Box plot with the 1.5 × IQR fence.* [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#percentiles).

**Example: PYQ (Sep 2023)**

Find the IQR of 14, 20, 40, 23, 18. Are there outliers?

1. Sorted: 14, 18, 20, 23, 40 (n = 5).
2. Q<sub>1</sub>: i = 0.25 × 5 = 1.25 → round up to 2 → 18.
3. Q<sub>3</sub>: i = 0.75 × 5 = 3.75 → round up to 4 → 23.
4. IQR = 5. Fences: 18 − 7.5 = 10.5 and 23 + 7.5 = 30.5.

**Answer:** IQR = 5, and 40 is an outlier

**Example: PYQ (May 2023)**

T-shirt prices: 150, 550, 700, 240, 300, 750, 200, 180, 320, 420. Find the price below which 25% fall, Q<sub>3</sub>, and the median.

1. Sorted: 150, 180, 200, 240, 300, 320, 420, 550, 700, 750 (n = 10).
2. Q<sub>1</sub>: i = 2.5 → 3rd value = 200.
3. Q<sub>3</sub>: i = 7.5 → 8th value = 550.
4. Median: i = 5 is whole → average of 5th and 6th = (300 + 320)/2 = 310.

**Answer:** Q₁ = ₹200, Q₃ = ₹550, median ₹310

**Example: PYQ (Jan 2023)**

Cars sold in five months: 12, 8, 9, 20, 40. Which values are outliers?

1. Sorted: 8, 9, 12, 20, 40. Q<sub>1</sub> = 2nd = 9, Q<sub>3</sub> = 4th = 20, IQR = 11.
2. Upper fence = 20 + 16.5 = 36.5; lower fence = 9 − 16.5 < 0.

**Answer:** 40

> [!WARNING]
> **Common traps**
> - Round **up** even when the decimal is small: 1.25 → 2, not 1.
> - Calculators and Excel use different quartile methods. Use the IITM steps above.
> - Q<sub>3</sub> separates the top 25% from the bottom 75%.
> - Box-plot whiskers end at the most extreme values that aren't outliers; outliers are drawn as dots.

<a id="two-categorical"></a>

## Week 4: Two categorical variables

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Joint relative frequency | cell/(grand total) |  |
| Row relative frequency | cell/(row total) |  |
| Column relative frequency | cell/(column total) |  |
| Marginal totals | row totals and column totals; each set adds to the grand total |  |

- Contingency (two-way) table: one variable on the rows, the other on the columns, counts in the cells, totals in the margins.
- Association: compare row percentages across the rows. If they are (nearly) the same in every row, there is no association.
- A stacked (or 100% stacked) bar chart shows those row percentages visually.

**Example: PYQ pattern (May 2024)**

200 people: 120 male, 80 female. 150 own a smartphone. 30 females don't own one. How many males own a smartphone?

1. Females who own = 80 − 30 = 50.
2. Males who own = 150 − 50 = 100 (so 20 males don't).

**Answer:** 100

*Diagram: The smartphone PYQ as a two-way table.* [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#two-categorical).

> [!TIP]
> Draw the empty table with its totals row and column first, write in every number given, then fill the blanks so each row and column adds up.

<a id="covariance"></a>

## Week 4: Scatter plots & covariance

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Sample covariance | (Σ(x<sub>i</sub> − x̅)(y<sub>i</sub> − y̅))/(n − 1) = (Σ x<sub>i</sub>y<sub>i</sub> − nx̅y̅)/(n − 1) |  |
| Population covariance | (Σ(x<sub>i</sub> − μ<sub>x</sub>)(y<sub>i</sub> − μ<sub>y</sub>))/n |  |
| Scaling | cov(ax + b, cy + d) = ac · cov(x, y) |  |
| With itself | cov(x, x) = Var(x) |  |

*Diagram: Why the sign of covariance works.* Each point adds (x − x̄)(y − ȳ). Points in the green quadrants push covariance up, points in the red ones pull it down. [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#covariance).

- Sign gives direction: positive (rise together), negative (one rises as the other falls), near 0 (no linear relation).
- Size depends on the units, so covariance can't measure strength. That's what correlation is for.
- Reading a scatter plot: direction, form (straight or curved), strength (how tightly points hug a line), outliers.

**Example**

x: 1, 2, 3 and y: 2, 4, 9. Find the population and sample covariance.

1. x̅ = 2, y̅ = 5.
2. Products of deviations: (−1)(−3) = 3, (0)(−1) = 0, (1)(4) = 4 → sum 7.
3. Population: 7 ÷ 3. Sample: 7 ÷ 2.

**Answer:** Population ≈ 2.33, sample = 3.5

> [!WARNING]
> **Common traps**
> - PYQs ask both kinds: 'population covariance' ⇒ ÷ n, 'sample covariance' ⇒ ÷ (n − 1).

<a id="correlation"></a>

## Week 4: Correlation coefficient (r)

*asked in every paper in past qualifier papers*

| | Formula | Note |
|---|---|---|
| Pearson r | r = (cov(x, y))/(s<sub>x</sub> s<sub>y</sub>) | Use sample values throughout, or population values throughout. Never mix. |
| Computational form | r = (nΣxy − ΣxΣy)/(√([nΣx² − (Σx)²][nΣy² − (Σy)²])) |  |
| Range | −1 ≤ r ≤ 1 |  |
| Change of origin and scale | r(ax + b, cy + d) = r(x, y) if ac > 0,  −r(x, y) if ac < 0 |  |

*Diagram: What r looks like.* r measures how tightly points hug a straight line. The U-shape has r = 0 even though y depends on x. [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#correlation).

**Reading r**

| r | Meaning |
|---|---|
| +1 or −1 | Perfect straight line, rising or falling |
| Close to ±1 | Strong linear association |
| Close to 0 | Weak or no **linear** association (could still be curved) |
| Sign | Direction only: + rising, − falling |

**Example: PYQ pattern (Jan 2023)**

Deepak scores exactly twice Mayur's marks in every subject (Y = 2X). What follows?

1. Y is a positive multiple of X, so the points lie on a rising straight line.

**Answer:** r = 1, cov(X, Y) = 2 Var(X), Var(Y) = 4 Var(X), SD(Y) = 2 SD(X), mean Y = 2 × mean X

> [!WARNING]
> **Common traps**
> - r measures how tightly the points hug a line, **not** how steep it is. A steep loose cloud has a smaller |r| than a shallow tight one.
> - Ordering scatter plots by r: strong negative < weak negative < none < weak positive < strong positive.
> - r = 0 doesn't mean no relationship: a U-shape can have r ≈ 0.
> - r has no units, so changing units (cm → m, ₹ → $) never changes it.
> - Correlation is not causation.

<a id="point-biserial"></a>

## Week 4: Point bi-serial correlation

*asked often in past qualifier papers*

| | Formula | Note |
|---|---|---|
| When | one variable is dichotomous (0/1: pass/fail, male/female), the other numerical |  |
| With sample SD | r<sub>pb</sub> = (Y̅<sub>1</sub> − Y̅<sub>0</sub>)/(s<sub>Y</sub>) × √((n<sub>1</sub>n<sub>0</sub>)/(n(n − 1))) |  |
| With population SD | r<sub>pb</sub> = (Y̅<sub>1</sub> − Y̅<sub>0</sub>)/(σ<sub>Y</sub>) × √((n<sub>1</sub>n<sub>0</sub>)/n²) | Same answer as the sample version. |
| Symbols | Y̅<sub>1</sub>, Y̅<sub>0</sub>: group means · n<sub>1</sub>, n<sub>0</sub>: group sizes · n = n<sub>1</sub> + n<sub>0</sub> · s<sub>Y</sub>, σ<sub>Y</sub>: SD of **all** Y values |  |

*Diagram: Hours studied, split by pass and fail.* The bigger the gap between the two group means (relative to the SD), the larger r<sub>pb</sub>. [View it on BTechi](https://www.btechi.in/qualifier/notes/stats-1#point-biserial).

**Example**

Hours studied: passed (coded 1): 6, 8, 7; failed (coded 0): 3, 4. Find r<sub>pb</sub>.

1. Y̅<sub>1</sub> = 7, Y̅<sub>0</sub> = 3.5, n<sub>1</sub> = 3, n<sub>0</sub> = 2, n = 5.
2. All Y: mean 5.6, Σ(y − y̅)² = 17.2, so s<sub>Y</sub> = √(17.2 ÷ 4) = 2.074.
3. r<sub>pb</sub> = 3.5/2.074 × √(6/20) = 1.688 × 0.548.

**Answer:** ≈ 0.925: strong positive association between hours studied and passing

> [!WARNING]
> **Common traps**
> - Pair the SD with the right root: sample SD ↔ n(n − 1); population SD ↔ n². Mixing them gives a wrong value.
> - Swapping which group is coded 1 flips the sign, which is why PYQs ask for the absolute value.

<a id="last-minute"></a>

## Last-minute checklist

- [ ] N-O-I-R: nominal → ordinal (order) → interval (equal gaps) → ratio (true zero).
- [ ] Numbers used as labels (PIN code, roll number) are categorical.
- [ ] Cross-sectional: many units, one time. Time-series: one unit, many times.
- [ ] Pie angle = f/n × 360°.
- [ ] Sample variance ÷ (n − 1), population ÷ n.
- [ ] y = ax + b: mean → ax̅ + b, variance → a² × var, SD → |a| × SD.
- [ ] Percentile: i = P × n / 100. Fraction → round up. Whole → average positions i and i + 1.
- [ ] Outliers lie beyond Q₁ − 1.5 × IQR or Q₃ + 1.5 × IQR.
- [ ] Wrong-value fixes: Σx² = (n − 1)s² + nx̅², then swap the value in both sums.
- [ ] r is unit-free, between −1 and 1, unchanged by positive scaling.
- [ ] r<sub>pb</sub> = (Y̅<sub>1</sub> − Y̅<sub>0</sub>) / s × √(n<sub>1</sub>n<sub>0</sub> / n(n − 1)).

---

From [BTechi](https://www.btechi.in), a free, independent study site for the IIT Madras BS. Not affiliated with IIT Madras. Found a mistake? [Open an issue](https://github.com/Btechi/iitm-bs-qualifier-notes/issues) or use the Report button on the [online sheet](https://www.btechi.in/qualifier/notes/stats-1).
