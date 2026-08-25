# Topic 3 — Model Training, Evaluation & Interpretation
### Lesson A · Introduction to Machine Learning · ITPU
**Format:** 60 min · 100% online (MS Teams) · 2nd-year CS/IT
**Prework:** students self-study the topic on the platform *before* class. This session is for engagement, gap-checking, the hard concepts, and hands-on coding — not lecturing from scratch.

---

## Session outcomes
By the end of the lesson students can:
1. **Describe what training a machine learning model involves.**
2. **Explain overfitting and underfitting** and recognize them when they occur.
3. **Interpret machine learning models and their predictions** (interpretability + SHAP).

---

## Lesson flow & resources

Each block lists the tool to open and how it is used. **No tool is used twice in this lesson.**

### 0 · Warm-up — diagnostic (Mentimeter)
- **Link:** https://www.mentimeter.com/app/presentation/al4281dc3bciy77o48s85amvffzoon9s/edit?question=h1mrymc9tgp8
- **Use:** "Confidence + Confusion" — a Scales question rating confidence on parameters/hyperparameters, overfitting, bias-variance, and SHAP, plus a Word Cloud "what confused you most?". The results tell you which concept to spend the most time on.

### 1 · What training involves (Excalidraw + HTML)
- **Excalidraw process flow:** https://excalidraw.com/#json=gWXH571Ujm1QmXMSRp_Ss,w1wOR8fp4fYCATL8gOMGTA
  (blank Excalidraw: https://excalidraw.com/)
  Shows the full ML pipeline (Data → Split → Model → **Training** → Evaluate → Predict) and zooms into the training loop (predict → measure loss → adjust → repeat).
- **Watch a Model Train (HTML):** `watch-a-model-train.html`
  Students watch the line fit and the loss shrink as `w` and `b` adjust; a learning-rate slider shows what a hyperparameter does. Pair with **TensorFlow Playground** (playground.tensorflow.org) for the "it scales automatically" moment.
- **Code moment:** `Topic3_Model_Training_Lab.ipynb` — the training loop in ~10 lines of NumPy; the same idea in code.

### 2 · Evaluate on unseen data (Colab)
- **Notebook:** `Topic3_Model_Training_Lab.ipynb` (Block 2)
  `train_test_split` on a deep tree → prints ~100% train vs much lower test accuracy. The **gap** is overfitting, made concrete.

### 3 · Overfitting / underfitting & bias-variance (HTML)
- **Bias–Variance Explorer (HTML):** `bias-variance-explorer.html`
  A complexity slider goes underfit → good fit → overfit, with live train vs test error and the classic U-shaped error curve. Preset buttons: Underfit (1) / Good fit (3) / Overfit (13).
- **Notebook (Block 3):** loops tree depth 1→20 and plots train vs test — mirrors the explorer in code.
- Optional: **TensorFlow Playground** live to "watch it overfit".

### 4 · Interpretability & SHAP (diagram + HTML + Colab)
- **Static diagram for slides:** `shap-diagram.png` — the restaurant-bill → force-plot analogy + how to read any SHAP plot.
- **SHAP Explorer (HTML):** `shap-explorer.html`
  Drag an apartment's features; each one pushes the predicted price up (green) or down (red) from the average — SHAP made tangible.
- **Notebook (Block 4):** feature-importance chart + a real **SHAP beeswarm** on a ready dataset.

### 5 · Concept check + case study (Miro)
- **Miro board:** https://miro.com/app/board/uXjVHuyI1Ps=/
  Team sort-and-match with four zones + hidden answer keys:
  1. Symptom → Diagnosis (overfitting / underfitting / good fit)
  2. High Bias vs High Variance
  3. Interpretable by design vs Needs SHAP
  4. Parameters vs Hyperparameters
  Includes a 10-min timer, breakout-rooms launcher, and a team-confidence scale.
- **Case study:** the "diagnose this model" scenarios in the notebook (Block 5) — given train/test scores, is it overfitting, underfitting, or a good fit, and what would you do?

---

## Files in this folder
| File | What it is |
|------|------------|
| `watch-a-model-train.html` | Interactive training-loop / gradient-descent explorer (offline) |
| `bias-variance-explorer.html` | Overfitting / bias-variance interactive explorer (offline) |
| `shap-explorer.html` | Interactive SHAP push-bars explorer (offline) |
| `shap-diagram.png` | Static SHAP analogy diagram for slides |
| `Topic3_Model_Training_Lab.ipynb` | Colab coding lab (training loop, train/test gap, bias-variance, SHAP, case study) |
| `sources for the lesson.docx` | Facilitator notes / source material |
| `README.md` | This file |

---

## How to run each resource
- **HTML files:** double-click to open in any browser (no internet needed). In Teams, share that browser tab. For a public link, publish via GitHub Pages.
- **Notebook:** open in Google Colab (File → Upload notebook) and run top to bottom, or share to breakout rooms for live coding. NumPy for the training loop; scikit-learn for the split/tree/importance demos; SHAP installs on first run.
- **Miro & Excalidraw:** open the board, start Live collaboration / a session, and paste the link into the Teams chat so students join.
- **Mentimeter:** open your Menti, present it, and share the join code/link in chat.

---

| Phase | Tool |
|-------|------|
| Warm-up | Mentimeter |
| What training involves | Excalidraw + Watch-a-Model-Train (HTML) + Colab |
| Evaluate on unseen data | Colab |
| Overfitting / bias-variance | Bias-Variance Explorer (HTML) |
| Interpretability / SHAP | SHAP diagram + SHAP Explorer (HTML) + Colab |
| Concept check + case study | Miro |

---

## Notes
- Links and local file paths (`C:/Users/user/Downloads/...`) should be verified before class.
- Reinforcement learning is **out of scope** for this course (named only).
- Topic 4 (Model Evaluation Strategies) is a separate 60-minute lesson with its own materials; a combined slide deck covers both.

Warm up:

https://www.mentimeter.com/app/presentation/ald281dc3bciy77o48s85amvffzoon9s/edit?question=h1mrymc9tgp8 



Training with HTML:
file:///C:/Users/user/Downloads/watch-a-model-train.html 

Explain training process:
https://excalidraw.com/#json=gWXH571Ujm1QmXMSRp_Ss,w1wOR8fp4fYCATL8gOMGTA 

https://excalidraw.com/

Overfitting underfitting
file:///C:/Users/user/Downloads/bias-variance-explorer.html

SHAP:
file:///C:/Users/user/Downloads/shap-explorer.html 


Task:
https://miro.com/app/board/uXjVHuyI1Ps=/ 

