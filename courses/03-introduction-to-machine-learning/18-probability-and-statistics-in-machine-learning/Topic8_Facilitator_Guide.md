# Topic 8 — Probability & Statistics in ML
## Facilitator Guide & Materials Pack (60-minute live session)

**Course:** Introduction to Machine Learning · **Platform:** MS Teams · **Cohort:** 25+ students (mixed level)
**Format:** Flipped — students have read the theory online. Live session = *diagnose → repair → apply*.
**The anchor idea:** *ML is decision-making under uncertainty; probability is how we measure that uncertainty.*

> **Tool variety note:** This session deliberately uses *different* tools from Topic 7 (Calculus). Topic 7 used a Mentimeter word cloud, Kahoot, a gradient-descent simulator, a derivative-family explorer, and a Miro plotting board. Topic 8 uses a **poll-and-reveal hook**, a **Mentimeter quiz + a custom distribution-match self-check**, three **new widgets** (Bayes tree, CLT simulator, correlation explorer), and a **shared verdict sheet** (Teams whiteboard / doc) with a **debate** mechanic.

---

## 0. What you need open before you start

| Tool | Purpose | Link/File |
|---|---|---|
| Slide deck | Main visual spine | `Topic8_Probability_Statistics.pptx` |
| Bayes Tree | Live demo (hook reveal + Fix #1) | `bayes_tree.html` |
| CLT Simulator | Live demo (Fix #3) | `clt_simulator.html` |
| Correlation Explorer | Live demo (Fix #2) | `correlation_causation.html` |
| Distribution-match widget | Diagnostic self-check | `distribution_match.html` |
| Poll (Teams or Mentimeter) | Hook vote + exit ticket | see §2, §6 |
| Mentimeter quiz | 8-question diagnostic | questions in §3 |
| Shared verdict sheet | Case study (Teams whiteboard / OneNote / shared doc) | template in §8 |
| MS Teams breakout rooms | 4 teams | "manually assign" |

---

## 1. Minute-by-minute run-sheet

| Time | Phase | You do | Students do | Slide |
|---|---|---|---|---|
| 0:00–0:03 | Intro | Welcome, agenda | Settle in | 1–2 |
| 0:03–0:05 | Hook | Launch the rare-disease poll | Vote A/B/C/D | 3 |
| 0:05–0:13 | Diagnostic quiz | 8 Menti Qs, tagged by bucket | Answer live | 4 |
| 0:13–0:20 | Distribution match | Run self-check widget | Match scenarios | 5 |
| 0:20–0:25 | Fix #1 Bayes | Bayes tree: reveal the hook answer | Watch, react | 6 |
| 0:25–0:29 | Fix #2 Cause | Correlation explorer, reveal stories | Guess the lurker | 7 |
| 0:29–0:32 | Fix #3 CLT | CLT sim: bell from chaos | Watch | 8 |
| 0:32–0:36 | Case setup | Explain A/B detective + traps | Understand | 9 |
| 0:36–0:44 | Breakout | Assign 4 teams different data; circulate | Compute + verdict | 10 |
| 0:44–0:50 | Reveal/debate | Teams defend; you reveal traps | Argue their call | 11 |
| 0:50–0:52 | Bridge | Connect to AutoCode tools | Listen | 11 |
| 0:52–0:56 | Exit ticket | Launch Forms/Menti | Answer 2 items | 12 |
| 0:56–1:00 | Wrap | Recap 4 takeaways, preview practice | — | 12 |

**If behind:** trim Fix #2 to 2 min (one example) and shorten the debate. Never cut the breakout.

---

## 2. The hook — "Your intuition lies" (Phase 1)

**Poll (Teams poll or Mentimeter):**
> A disease affects 1 in 100 people. A test is 99% accurate. You test POSITIVE.
> What's the chance you're actually sick?
> **A) ~99%  B) ~90%  C) ~50%  D) ~1%**

Most vote **A**. Reveal the correct answer is **C (~50%)** — but do **NOT** explain yet.
> "Hold that thought. Your gut says 99%. The truth is about 50%. We'll see exactly why in a few minutes — and this gap is the whole reason ML uses math instead of instinct."

This creates suspense that Fix #1 (the Bayes tree) pays off.

---

## 3. Diagnostic quiz — full bank (Phase 2)

Run 8 questions in **Mentimeter** (different from Topic 7's Kahoot). Each is tagged to one of 4 buckets. After the quiz, the **weakest bucket(s)** = what you teach in Phase 3. ✓ = correct.

**BUCKET 1 — Probability foundations**

**Q1.** Two events are *independent* when…
- A) they can't happen together
- B) knowing one tells you nothing about the other ✓
- C) they have the same probability
- D) they always happen together

**Q2.** Conditional probability P(A|B) means…
- A) probability of A and B both
- B) probability of A, given that B happened ✓
- C) probability of B, given A
- D) probability of A or B

**BUCKET 2 — Bayes & distributions**

**Q3.** Bayes' theorem lets us…
- A) prove causation
- B) update a probability after seeing evidence ✓
- C) eliminate all uncertainty
- D) compute an average

**Q4.** Which is a *continuous* distribution?
- A) Bernoulli
- B) Binomial
- C) Gaussian (Normal) ✓
- D) Poisson

**Q5.** The number of emails arriving per hour is best modeled by…
- A) Gaussian
- B) Poisson ✓
- C) Uniform
- D) Bernoulli

**BUCKET 3 — Descriptive vs inferential**

**Q6.** A *p-value* tells you…
- A) the probability your hypothesis is true
- B) roughly, how surprising the data would be if there were no real effect ✓
- C) the size of the effect
- D) the sample size needed

**Q7.** The *median* is preferred over the *mean* when data…
- A) is perfectly symmetric
- B) has extreme outliers / is skewed ✓
- C) is very large
- D) is categorical

**BUCKET 4 — ML traps**

**Q8.** "Correlation does not imply causation" means…
- A) correlated variables are never related
- B) a relationship in data may be driven by a hidden common cause ✓
- C) correlation is always wrong
- D) causation is impossible to establish

**Optional extras (strong cohort):**

**Q9.** The Law of Large Numbers says that as sample size grows, the sample mean…
- A) gets further from the true mean
- B) approaches the true mean ✓
- C) becomes random
- D) stays the same

**Q10.** A model trained on a biased sample will most likely…
- A) generalize perfectly
- B) reproduce that bias on new data ✓
- C) fix the bias automatically
- D) have no effect

### Distribution-match self-check (immediately after)
Open `distribution_match.html`. Students drag each scenario to its distribution. This is a fast, hands-on check of the most-testable, most-confused piece. Read who struggles → informs Fix depth.

---

## 4. Targeted explanation cues (Phase 3)

Teach the weakest bucket(s) from the diagnostic. These three fixes are reliably needed:

### Fix #1 — Bayes without the fear (slide 6, `bayes_tree.html`)
This is the **payoff of the hook.**
1. Open the tree at prevalence = 1%, sensitivity = 99%, specificity = 99%. Point at the bottom bar: ~10 true positives vs ~10 false positives → **~50%**. *"There's your answer from the poll."*
2. Slide prevalence up to 10%, then 30%. The "chance you're sick" climbs. *"Rarer disease → false positives from the huge healthy group swamp the few true positives."*
3. **Only now** click "Show Bayes' formula." The intuition earns the formula.
4. ML tie-in: *"This is exactly why we care about precision/recall and class imbalance — a rare positive class behaves just like a rare disease."*

### Fix #2 — Correlation ≠ causation (slide 7, `correlation_causation.html`)
Click through the tabs. For each, ask the room *"what's the hidden cause?"* before hitting **Reveal the real story.**
- Ice cream ↔ drownings → summer heat
- Shoe size ↔ reading → age
- Fire trucks ↔ damage → fire size
- The "pure coincidence" tab makes the spurious-correlation point.
ML tie-in: *"Models exploit correlation to predict — and break when the lurking variable shifts. Correlation predicts; causation explains."*

### Fix #3 — The CLT (slide 8, `clt_simulator.html`)
1. Pick the **bimodal** (two-hump) source — the least bell-like option.
2. Click **+500 fast**. A bell emerges; the green normal curve fits.
3. Raise **n** and redraw — the bell tightens.
Say: *"The averages go normal no matter how weird the source. That's why confidence intervals work and why more data = more stable estimates."* → motivates AutoCode exercise #1 (confidence intervals).

---

## 5. Case study — "The A/B Test Detective" (Phase 4)

### Facilitator answer key (the planted traps)

Each team decides **SHIP** or **DON'T SHIP** and must name the trap. Click-through rate (CTR) = clicks ÷ impressions.

**Team 1 — clean control**
- A: 100/1000 = 10.0% · B: 130/1000 = 13.0%
- Both samples large (n=1000). A 3-point lift is real and stable. **Verdict: SHIP.** (No trap — this is the honest baseline so at least one team gets a clean "yes.")

**Team 2 — sample-size trap**
- A: 100/1000 = 10.0% · B: 13/100 = 13.0%
- B *looks* identical to Team 1's B (13%), but n=100 is tiny → the estimate could easily be 8% or 18%. **Verdict: DON'T SHIP yet — collect more data.** Trap: small sample = wide uncertainty.

**Team 3 — noise trap**
- A: 100/1000 = 10.0% · B: 108/1000 = 10.8%
- Difference is 0.8 points on n=1000 — well within random noise; not significant. **Verdict: DON'T SHIP.** Trap: a difference that isn't statistically meaningful.

**Team 4 — Simpson's paradox trap**
- Aggregate: B has the higher overall CTR.
- But split by segment (e.g., mobile vs desktop), **A wins in every segment** — B only looks better because its traffic mix is weighted toward the easy-to-convert segment. **Verdict: DON'T SHIP / investigate segments.** Trap: aggregate reverses when you condition on a variable.

*(Concrete numbers for Team 4, if you want to hand them out:*
*Mobile — A: 90/100 (90%), B: 380/500 (76%). Desktop — A: 100/900 (11%), B: 5/500 (1%).*
*Aggregate — A: 190/1000 (19%), B: 385/1000 (38.5%). B "wins" overall, loses every segment.)*

### The reveal & debate (slide 11)
Each team **defends first**, then you reveal. The meta-lesson:
> "A bigger number is not a better model. Sample size, statistical significance, and hidden structure decide — and those are exactly what your AutoCode tools measure."

Bridge to practice: confidence intervals (Team 2's uncertainty), chi-squared & KS tests (Team 3's 'is it real?'), ECDF (comparing whole distributions, not just averages).

---

## 6. Wrap-up & exit ticket (Phase 5)

**Exit ticket** (MS Forms / Mentimeter — responses feed your next session):
1. *(conceptual)* A rare-disease test is 99% accurate and you test positive — why isn't your risk 99%? *Expected: because the disease is rare, false positives from the large healthy group are comparable to (or exceed) the true positives, so P(sick | positive) is far below the test's accuracy.*
2. *(muddiest point, open text)* What's still unclear?

**Recap the 4 takeaways** (slide 12), then point to **AutoCode practice**:
1. Confidence intervals 2. ECDF 3. Chi-squared test 4. Two-sample Kolmogorov–Smirnov test
Reassure them: some concepts weren't fully drilled today — the ReadMe covers what's needed.

---

## 7. STUDENT HANDOUT — Diagnostic distribution match
*(if you prefer paper/chat over the widget)*

> Match each scenario to ONE distribution: *Bernoulli · Binomial · Poisson · Gaussian · Uniform · Exponential*
> 1. A single coin flip (heads/tails) → ____
> 2. Number of heads in 10 flips → ____
> 3. Number of customer calls per hour → ____
> 4. Heights of adult women → ____
> 5. A random number equally likely between 0 and 1 → ____
> 6. Time you wait for the next bus → ____
>
> *(Answers: 1 Bernoulli · 2 Binomial · 3 Poisson · 4 Gaussian · 5 Uniform · 6 Exponential)*

---

## 8. STUDENT HANDOUT — A/B Test Detective (CLEAN — no answers)
*(paste the relevant team's block into that breakout room's chat. Do NOT show slide 10's italic labels — those are the answers.)*

> ### 🕵️ The A/B Test Detective
> Your team is deciding whether to ship **Model B** (new) over **Model A** (current).
> CTR = clicks ÷ impressions.
>
> **Your team's data:**
>
> - **Team 1** — A: 100 clicks / 1000 shown · B: 130 / 1000
> - **Team 2** — A: 100 / 1000 · B: 13 / 100
> - **Team 3** — A: 100 / 1000 · B: 108 / 1000
> - **Team 4** — Overall: A 190/1000, B 385/1000. *By segment* → Mobile: A 90/100, B 380/500 · Desktop: A 100/900, B 5/500
>
> **On the shared verdict sheet, answer:**
> 1. What is each model's click-through rate?
> 2. Your verdict: **SHIP B** or **DON'T SHIP B**?
> 3. What's the catch? Name the statistical trap (if any) in your data.
>
> ⏱️ 8 minutes. Pick a spokesperson to defend your verdict.

---

## 9. Shared verdict sheet (Teams whiteboard / OneNote / Google Doc) — setup

Create one page with a 4-row table, one row per team:

| Team | CTR of A | CTR of B | Verdict (SHIP / DON'T) | The trap we found |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |

Teams fill their row live. During the reveal, the filled table makes the disagreement visible at a glance — that contrast is the teaching moment.

---

## 10. Facilitator cheat-answers (rapid Q&A)

- **"Why is the rare-disease answer ~50%, not 99%?"** → Of 1000 people, 10 are sick (≈10 true positives) but 990 healthy × 1% error ≈ 10 false positives. Positives ≈ 20, half truly sick.
- **"What makes a difference 'significant'?"** → Roughly, that it's larger than what random sampling noise would produce; formal tools: p-values, confidence intervals, chi-squared/KS tests.
- **"Discrete vs continuous distribution?"** → Discrete = countable outcomes (coin, dice, counts): Bernoulli/Binomial/Poisson. Continuous = any value in a range (heights, time): Gaussian/Uniform/Exponential.
- **"Isn't correlation useful then?"** → Yes — it's enough to *predict*. You need causation to *intervene* or to trust a model when conditions change.
- **"What's Simpson's paradox again?"** → A trend that appears in aggregated data reverses when you split into subgroups, because of an unequal mix across groups.
- **"Why does the CLT matter for ML?"** → It underpins confidence intervals, many significance tests, and the intuition that more data → more stable estimates.
