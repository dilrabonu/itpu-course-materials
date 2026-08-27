# Topic 4 — Model Evaluation Strategies
### Lesson B · Introduction to Machine Learning · ITPU
**Format:** 60 min · 100% online (MS Teams) · 2nd-year CS/IT
**Prework:** students self-study the topic on the platform *before* class. This session is for engagement, gap-checking, the hard concepts, and hands-on coding — not lecturing from scratch.

---

## Session outcomes
By the end of the lesson students can:
1. **Describe cross-validation techniques** used to evaluate ML models.
2. **Calculate metrics to evaluate classification models** (accuracy, precision, recall, F1, ROC-AUC).
3. **Calculate metrics to evaluate regression models** (MSE/RMSE, MAE, MAPE, sMAPE, R²).

---

## Lesson flow & resources

Each block lists the tool to open and how it is used. **No tool is used twice in this lesson**, and the tools differ from Topic 3 so nothing feels repeated.

### 0 · Warm-up — gamified reading check (Kahoot)
- **Play link:** https://create.kahoot.it/share/topic-4-warm-up/8aa29cfc-6d57-4ffa-8598-978da7fa691e
- **Edit link:** https://create.kahoot.it/my-library/kahoots/a73fb07a-b955-498b-9531-649b2442a1cf
- **Use:** a 10-question competitive quiz on the async reading (cross-validation + metrics). Host live, share the game PIN in the Teams chat. Reveals what stuck and warms up the class.

### 1 · Cross-validation strategies (Excalidraw)
- **Board:** https://excalidraw.com/#json=xfKwsjY_kcfkwwnTvmNLz,jG4BMyB2rFSiWHCcMiri4w
  (blank Excalidraw: https://excalidraw.com/)
- **Use:** the five strategies drawn as train/validate fold grids — K-Fold, Leave-One-Out, Stratified, Grouped, Time-Series — revealed one at a time. Ask the engaging question before each reveal: *which strategy for time-dependent / imbalanced / grouped data?*
- **Backup (HTML):** `cross-validation-visualizer.html` — the same five strategies as clickable tabs with a K slider, for exploration. Open locally in a browser.

### 2 · Classification & regression metrics (Wooclap)
- **Live session:** https://app.wooclap.com/events/GBNJUGS/live-session
- **Use:** LaTeX-rendered multiple-choice questions on precision, recall, F1, RMSE, MAE, R², plus start/end confidence ratings. Ideal for the math-heavy part. Share the join code in the Teams chat.

### 3 · Concept check — sort & match (Miro)
- **Board:** https://miro.com/app/board/uXjVHuyI1Ps=/
- **Use:** the Topic 4 section (three sorting zones + hidden answer keys):
  1. Dataset → which cross-validation strategy?
  2. Scenario → which metric matters most? (recall vs precision vs regression)
  3. Classification metric vs Regression metric (two-column sort)
  Includes a 10-min timer, breakout-rooms launcher, and a team-confidence scale.

### 4 · Coding lab (Google Colab)
- **Notebook:** `Topic3_and_4_ML_Lab.ipynb` — one continuous notebook from Topic 3; Topic 4 half has the three AutoCode exercises.
- **Exercises (NumPy only, broken/blank code + self-check + hidden solution):**
  1. Classification metrics (accuracy, precision, recall, F1)
  2. Regression metrics (MSE, RMSE, MAE, MAPE, R²)
  3. Cross-validation splits (K-fold & time-series indices)
- **Practice note:** these are auto-checked in **AutoCode** by unit tests. NumPy refresher: https://cs231n.github.io/python-numpy-tutorial/#numpy

### 5 · Wrap-up — exit ticket (MS Forms)
- **Use:** an anonymous 5-question exit ticket in Teams — two confidence ratings, one quick knowledge check (time-series strategy), one "what to revisit", one open reflection. Use the responses to plan the next session. Remind students to submit their three AutoCode exercises.

---

## Files in this folder
| File | What it is |
|------|------------|
| `cross-validation-visualizer.html` | Interactive 5-strategy CV visualizer (offline backup) |
| `Topic3_and_4_ML_Lab.ipynb` | Combined Colab lab — Topic 4 half has the 3 AutoCode exercises |
| `README.md` | This file |

*(The combined slide deck `ITPU-ML-Topics-3-4.pptx` covers both Topic 3 and Topic 4.)*

---

## How to run each resource
- **Kahoot:** open the play link → Host → share the game PIN in Teams chat.
- **Excalidraw:** open the board link → Live collaboration → paste the link into Teams. Reveal strategies one at a time.
- **HTML file:** double-click to open in any browser (no internet needed); share that browser tab in Teams.
- **Wooclap:** open the live session → share the join code/link in Teams; advance question by question.
- **Miro:** open the board → scroll to the Topic 4 section → Live collaboration → launch breakout rooms + timer.
- **Colab:** open the notebook (File → Upload notebook), run top to bottom, or share to breakout rooms.
- **MS Forms:** create the exit ticket, set to anonymous, paste the link in Teams at ~55 min.

---

| Phase | Tool |
|-------|------|
| Warm-up | Kahoot |
| CV strategies | Excalidraw (HTML visualizer as backup) |
| Metrics | Wooclap |
| Concept check | Miro |
| Coding | Google Colab |
| Wrap-up | MS Forms |

---

## Resources (for deeper reading / Q&A prep)
- Interpretable ML book — https://christophm.github.io/interpretable-ml-book/
- Google ML Crash Course — https://developers.google.com/machine-learning/crash-course
- NumPy tutorial (for the coding exercises) — https://cs231n.github.io/python-numpy-tutorial/#numpy

---

## Notes
- Links and local file paths (`C:/Users/user/Downloads/...`) should be verified before class.
- The coding notebook is shared with Topic 3 — students continue in the same file, so evaluation flows straight out of training.
- Topic 3 (Model Training, Evaluation & Interpretation) is the preceding 60-minute lesson with its own materials; the combined slide deck covers both.


Kahoot - warm up
https://create.kahoot.it/share/topic-4-warm-up/8aa29cfc-6d57-4ffa-8598-978da7fa691e 

https://create.kahoot.it/my-library/kahoots/a73fb07a-b955-498b-9531-649b2442a1cf 

Strategies Excalidraw

https://excalidraw.com/#json=xfKwsjY_kcfkwwnTvmNLz,jG4BMyB2rFSiWHCcMiri4w 
https://excalidraw.com/
HTML:
Croos validation
file:///C:/Users/user/Downloads/cross-validation-visualizer.html 


Metrics Wooclap
https://app.wooclap.com/events/GBNJUGS/live-session 

Miro sort

https://miro.com/app/board/uXjVHuyI1Ps=/  

coding

Warp up

Resources

https://christophm.github.io/interpretable-ml-book/


https://developers.google.com/machine-learning/crash-course 