# Breakout Room Brief — "Spot the Bug" (20 min)

Your room has ONE notebook to fix together: **stage4_spot_the_bug.ipynb**
There are **4 bugs**. Work as a team, not alone.

---

## FIRST (2 min)
1. Open the notebook in Colab → **File → Save a copy in Drive** (so you edit your own).
2. Assign roles (rotate the Driver after bug 2):
   - **Driver** – shares screen, types the fixes
   - **Navigator** – reads the error out loud, suggests what to change
   - **Explainer** – writes your one-sentence "why" for each bug
   - **Reporter** – posts your 4 sentences in the main chat at the end
3. Run the **setup cell** (don't change it).

---

## THE LOOP — do this for each of the 4 bugs
1. **Run** the cell.
2. **Read** the error, or check why the number is wrong.
3. **Find** the ONE line that's wrong.
4. **Fix** it and re-run until it's correct.
5. **Say why** in one sentence — the Explainer writes it down.

Work top to bottom. Bugs get harder as you go.

---

## WHAT TO WATch FOR
- **Bugs 1 and 3 CRASH** — a red error tells you something's wrong.
- **Bugs 2 and 4 run SILENTLY but give the wrong answer** — these are the
  sneaky ones. The number is just wrong; no error warns you.
  (In real projects, the silent ones are the dangerous ones.)

---

## YOUR DELIVERABLE (post in main chat at the end)
Four short lines, one per bug:
```
Bug 1: was ___ , wrong because ___
Bug 2: was ___ , wrong because ___
Bug 3: was ___ , wrong because ___
Bug 4: was ___ , wrong because ___
```

---

## FINISHED EARLY? Stretch question
Bug 1: someone "fixes" it with `A ** 2` or `np.square(A)` and it still looks
wrong. Why? What are the TWO correct ways to square a matrix?
(Answer to discuss: `**2` and `np.square` are also element-wise. Only
`A @ A` or `np.linalg.matrix_power(A, 2)` do a real matrix square.)
