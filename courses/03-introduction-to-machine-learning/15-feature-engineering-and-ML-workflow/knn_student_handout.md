# KNN Activity — ML Playground
## "Which K would you trust?"

Tool: **ml-playground.com** → click **K Nearest Neighbors**

---

## HOW TO PLACE POINTS
1. Click the **orange** square (top of the panel) to select the orange class.
2. Click on the white canvas to drop orange points.
3. Click the **purple** square, then drop purple points.
4. Set **K** in the Parameters box, then click **Train**.
5. The background fills with colored regions — that is the decision boundary.

You are copying a *pattern*, not exact pixels. Just keep the two groups
in the same corners and put the one troublemaker where shown.

---

## MAIN ACTIVITY — LAYOUT A (two clusters + 1 troublemaker)

Place **6 ORANGE** points in the UPPER-LEFT area (a loose cluster).
Place **6 PURPLE** points in the LOWER-RIGHT area (a loose cluster).
Then place **1 ORANGE** point INSIDE the purple cluster  ← the troublemaker.

```
    012345678901234567890
 2  ......O
 3  ....O
 4  ........O
 5  ...O.O
 7  .......O                <- orange cluster (upper-left)
 9                   P
11                   P
13               P X        <- X = the ORANGE troublemaker in purple zone
14                  P
15              P P         <- purple cluster (lower-right)
```

### THE EXPERIMENT — change ONLY K, retrain each time
Watch the area AROUND the troublemaker point.

| Set K = | Click | What you should see | Meaning |
|---------|-------|--------------------|---------|
| 1  | Train | small ORANGE island around the lone point | trusts noise = OVERFIT |
| 3  | Train | island shrinks / wobbles | vote starts to outweigh it |
| 7  | Train | island GONE, clean boundary | ignores noise = GENERALIZES |

### DISCUSS (answer in chat BEFORE the teacher explains)
- That troublemaker was probably a mislabeled point (noise).
- Which K **obeyed** it? Which K **ignored** it?
- New data is coming. **Which K do you trust — and why?**

---

## WARM-UP — LAYOUT B (clean split, no troublemaker)
7 orange upper-left, 7 purple lower-right, well separated. Train at K=3.
You get a clean diagonal boundary. This is what "easy and correct" looks like.

## CHALLENGE — LAYOUT C (mixed blobs)
Put the clusters closer, with 2 points of each color leaking into the other
side. Train at K=1, 3, 7. Notice: NO value of K gives a perfect line.
Lesson: real data is messy — you pick the best tradeoff, not perfection.

---

## THE ONE SENTENCE TO REMEMBER
Small K obeys every point, including the noise (overfitting).
Larger K lets the neighborhood vote, ignoring odd points (generalizing).
You choose K by which one you'd trust on data you have NOT seen yet.
