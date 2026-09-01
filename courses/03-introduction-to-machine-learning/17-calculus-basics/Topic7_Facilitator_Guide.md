# Topic 7 — Calculus Basics
## Facilitator Guide & Materials Pack (60-minute live session)

**Course:** Introduction to Machine Learning · **Platform:** MS Teams · **Cohort:** 25+ students (mixed level)
**Format:** Flipped — students have read the theory online. Live session = *diagnose → repair → apply*.
**The one idea to land:** *Gradient descent = walking downhill on a loss surface.*

---

## 0. What you need open before you start

| Tool | Purpose | Link/File |
|---|---|---|
| Slide deck | Main visual spine | `Topic7_Calculus_Basics.pptx` |
| Gradient Descent Simulator | Live demo (Phases 3 & 4) | `gradient_descent_simulator.html` |
| Derivative Family Explorer | Optional, Fix #3 | `derivative_family_explorer.html` |
| Mentimeter | Word cloud (hook) + confidence scales + exit ticket | pre-build from §3 |
| Kahoot **or** Mentimeter Quiz | 6-question diagnostic | questions in §4 |
| Miro **or** Excalidraw board | Breakout gradient-descent trails | template in §7 |
| MS Teams breakout rooms | 4–5 rooms of ~5 | set up "manually assign" |

> **Tip:** open both HTML widgets in browser tabs before the call. Share the *browser window*, not the whole screen, so students don't see your notes.

---

## 1. Minute-by-minute run-sheet

| Time | Phase | You do | Students do | Slide |
|---|---|---|---|---|
| 0:00–0:03 | Intro | Welcome, one-line agenda | Settle in | 1–2 |
| 0:03–0:05 | Hook | Launch Menti word cloud, read mood aloud | Type one word | 3 |
| 0:05–0:13 | Diagnostic quiz | Run 6 Kahoot Qs; show distribution after each | Answer live | 4 |
| 0:13–0:20 | Confidence check | Menti 1–5 scales; overlay vs quiz | Self-rate | 4 |
| 0:20–0:24 | Fix #1 | Simulator: slope→gradient→minus sign | Watch, answer "which way downhill?" | 5 |
| 0:24–0:28 | Fix #2 | Simulator: sweep learning rate | Watch it crawl/converge/explode | 6 |
| 0:28–0:32 | Fix #3 | Derivative-family table (widget optional) | Ask questions | 7 |
| 0:32–0:36 | Case setup | Explain f(x)=(x−3)², the 3-step loop | Understand task | 8 |
| 0:36–0:44 | Breakout | Assign rooms w/ different α; circulate | Compute + plot 3 steps | 9 |
| 0:44–0:50 | Reveal | Each room reports; narrate the pattern | Report trajectory | 10 |
| 0:50–0:52 | Bridge | Connect to real ML + AutoCode | Listen | 11 |
| 0:52–0:56 | Exit ticket | Launch Forms/Menti | Answer 2 items | 12 |
| 0:56–1:00 | Wrap | Recap 4 takeaways, preview practice | — | 12 |

**Timing buffers:** if you're behind, cut Fix #3 to 2 min (table only) and trim breakout report-back. Never cut the breakout itself — it's the learning core.

---

## 2. The hook (Phase 1)

**Mentimeter word cloud.** Question: *"In ONE word — how do you feel about calculus in ML?"*

- Read 4–5 words aloud. If anxious words dominate ("scary", "hard", "confusing"), say:
  > "I see a lot of nervous words. Here's my promise: by the end of the hour, this stops being scary and becomes *mechanical* — a recipe you follow."
- If confident words dominate, raise the stakes:
  > "Great — then the quiz will be a nice warm-up, and the case study will still surprise you."

---

## 3. Diagnostic quiz — full question bank (Phase 2)

Run 6 questions live (Kahoot for gamified leaderboard with 25+, or Mentimeter). **After each question, display the answer distribution** — that pattern is your gap map. Any question with >40% wrong: pause 20 seconds and address it immediately.

Correct answers marked ✓. Each question is tagged to a concept so results tell you where to teach.

**Q1 — [Derivative]** A derivative measures…
- A) the area under a curve
- B) the rate at which a function's output changes ✓
- C) the largest value a function reaches
- D) the average of all outputs

**Q2 — [Gradient direction]** The gradient ∇f points in the direction of…
- A) steepest descent (downhill)
- B) steepest ascent (uphill) ✓
- C) the nearest minimum
- D) zero change

**Q3 — [Gradient descent]** In gradient descent, we update parameters by moving in the direction of…
- A) the positive gradient
- B) the negative gradient ✓
- C) the second derivative
- D) a random direction

**Q4 — [Partial derivative]** We use a *partial* derivative when the function has…
- A) only one input
- B) multiple inputs, and we vary one at a time ✓
- C) no minimum
- D) a matrix output

**Q5 — [Hessian]** The Hessian is a matrix of…
- A) first-order partial derivatives
- B) second-order partial derivatives ✓
- C) function values
- D) learning rates

**Q6 — [Practical / local minima]** The main risk of plain gradient descent is…
- A) it always finds the global minimum
- B) it can get stuck in a local minimum ✓
- C) it never converges
- D) it requires no learning rate

**Optional extra (if time / strong cohort):**

**Q7 — [Jacobian]** The Jacobian is used for functions that map…
- A) one number to one number
- B) many numbers to one number
- C) a vector to a vector ✓
- D) a matrix to a scalar

**Q8 — [Learning rate]** If the learning rate α is far too large, gradient descent will…
- A) converge faster with no downside
- B) overshoot and possibly diverge ✓
- C) stop immediately
- D) turn into a derivative

### Confidence check (immediately after)
Mentimeter **scales** (1 = "no idea" → 5 = "could teach it") for: *Derivative · Partial derivative · Gradient · Jacobian · Hessian · Gradient descent*.

**Read the overlay:** the danger zone is **high confidence + low quiz accuracy**. Teach those first in Phase 3.

---

## 4. Targeted explanation cues (Phase 3)

Only teach what the diagnostic exposed. These three are almost always needed:

### Fix #1 — Gradient as a compass (slide 5, simulator)
1. Open the simulator with `f(x)=(x−3)²`, start x₀ = 8.
2. Point at the orange tangent line: *"the slope here is steep and positive — that's the gradient."*
3. Click **One Step** twice. *"See how the slope flattens as we near the bottom? At the minimum the gradient is zero."*
4. Hammer the minus sign: *"gradient points uphill; the minus in `x ← x − α∇f` is what sends us downhill."*

### Fix #2 — The learning-rate trap (slide 6, simulator)
Keep x₀ fixed, sweep the α slider and **Auto-Run** each time:
- α = 0.05 → *crawls* (slow but correct)
- α = 0.3 → *converges cleanly* (the goal)
- α = 1.1 → *explodes* (diverges to infinity)

Say: *"Same algorithm. One number. That number is the difference between a model that trains and one that blows up."*

### Fix #3 — Which derivative when (slide 7, optional widget)
Use the table. If confusion is high, open `derivative_family_explorer.html` and click each card. The three sentences that fix 90% of confusion:
- **Gradient** = a *vector* of all partial derivatives.
- **Jacobian** = a *matrix*, for functions that output a vector.
- **Hessian** = *second-order*; tells you min vs max vs saddle.

---

## 5. Case study — "Roll the Ball Downhill" (Phase 4)

### Facilitator version (with the answer key)

**Function:** f(x) = (x−3)²  **Gradient:** f′(x) = 2(x−3)  **Minimum:** x = 3
**Update rule:** x ← x − α·f′(x), starting x₀ = 8.

**Worked trajectories (what each room should get):**

**Room 1 — α = 0.1** (converges slowly)
| Step | x | f′(x)=2(x−3) | new x = x − 0.1·f′ |
|---|---|---|---|
| 0 | 8.00 | 10.00 | 7.00 |
| 1 | 7.00 | 8.00 | 6.20 |
| 2 | 6.20 | 6.40 | 5.56 |
→ marching steadily toward 3. Would take ~30 steps to arrive.

**Room 2 — α = 0.5** (converges fast — the sweet spot)
| Step | x | f′(x) | new x |
|---|---|---|---|
| 0 | 8.00 | 10.00 | 3.00 |
| 1 | 3.00 | 0.00 | 3.00 |
| 2 | 3.00 | 0.00 | 3.00 |
→ reaches the minimum in ONE step here (because α=0.5 is exactly right for this curve). Great "wow" moment.

**Room 3 — α = 0.9** (overshoots, wobbles)
| Step | x | f′(x) | new x |
|---|---|---|---|
| 0 | 8.00 | 10.00 | −1.00 |
| 1 | −1.00 | −8.00 | 6.20 |
| 2 | 6.20 | 6.40 | 0.44 |
→ zig-zags across the valley (overshoots past 3 each time) but slowly shrinks toward 3.

**Room 4 — α = 1.1** (diverges — explodes)
| Step | x | f′(x) | new x |
|---|---|---|---|
| 0 | 8.00 | 10.00 | −3.00 |
| 1 | −3.00 | −12.00 | 10.20 |
| 2 | 10.20 | 14.40 | −5.64 |
→ each step gets *further* from 3. Loss grows without bound. **This is the highlight of the reveal.**

### The reveal (slide 10)
Have each room drop their (x, loss) trail on the shared board. Then narrate:
> "Rooms 1 and 2 found the minimum. Room 3 wobbled but survived. Room 4 exploded. Same code, same starting point — only α changed. **That's why the learning rate is the single most important hyperparameter to tune.**"

Bridge: *"Your AutoCode gradient-descent exercise is exactly this loop — just generalized to a vector of parameters."*

---

## 6. Wrap-up & exit ticket (Phase 5)

**Exit ticket** (MS Forms or Mentimeter — collect responses, they feed your next session):
1. *(conceptual)* Why do we step in the **negative** gradient direction? — *Expected: the gradient points uphill/toward steepest ascent, so its negative points downhill toward lower loss.*
2. *(muddiest point, open text)* What's still unclear?

**Recap the 4 takeaways** (slide 12), then point to the **AutoCode practice**:
1. Derivatives, partial derivatives & gradients
2. Gradient descent
3. Mini-batch gradient descent
Remind them: auto-checked by unit tests; the ReadMe covers anything not in the lecture.

---

## 7. STUDENT HANDOUT — Breakout worksheet
*(paste into Teams chat / the shared board as the breakout starts)*

> ### 🎯 Your mission: roll the ball downhill
> **Function:** f(x) = (x − 3)²  **Gradient:** f′(x) = 2(x − 3)
> **Your room's learning rate α and start x₀ are on the slide.**
>
> Do **3 steps** of gradient descent. Fill the table:
>
> | Step | current x | gradient = 2(x−3) | new x = x − α × gradient |
> |---|---|---|---|
> | 0 | (x₀) | | |
> | 1 | | | |
> | 2 | | | |
>
> Then on the shared board:
> 1. Plot your 3 points on the curve.
> 2. In one word, how did your run behave? (converged / wobbled / exploded)
> 3. Pick one person to report back.
>
> ⏱️ 7 minutes.

---

## 8. Shared board (Miro / Excalidraw) — setup instructions

Create one frame with:
- A pre-drawn parabola f(x)=(x−3)² with the x-axis labelled −6 to 12, minimum marked at x=3.
- Four coloured sticky-note columns: **Room 1 (α=0.1)**, **Room 2 (α=0.5)**, **Room 3 (α=0.9)**, **Room 4 (α=1.1)**.
- Each room drops dots for their x-values along the curve + a one-word behaviour label.

*If short on prep time:* Excalidraw is faster — just draw the parabola, add 4 labelled boxes, share the collaboration link in chat. The comparison across columns during the reveal is the whole point.

---

## 9. Facilitator cheat-answers (rapid Q&A)

- **"Why not just solve f′(x)=0 directly?"** → For one variable you can. Real models have millions of parameters and no closed-form solution, so we descend iteratively.
- **"What's a good learning rate?"** → No universal value; it depends on the loss surface. In practice you tune it (or use adaptive optimizers like Adam).
- **"What's the difference between GD and SGD?"** → GD uses the whole dataset per step; SGD/mini-batch uses a small random sample — faster, and the noise helps escape local minima.
- **"Is the Hessian used in training?"** → Rarely directly (too big), but it underlies second-order methods and explains convexity/curvature.
- **"Local vs global minimum?"** → A local min is lowest in its neighbourhood; the global min is lowest overall. Plain GD can get stuck in a local min.
