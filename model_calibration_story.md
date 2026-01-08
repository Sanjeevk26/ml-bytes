# Model Calibration  
## Accuracy vs Calibration Using a Weather App

Machine learning models often output probabilities.

For example:
- “There is an 80% chance of rain today”
- “There is a 30% chance of rain tomorrow”

At first glance, these numbers seem straightforward.  
But two very different questions are hidden inside them.

1. Did the model predict the outcome correctly?
2. Did the model’s confidence match reality?

These questions correspond to **accuracy** and **calibration**.

---

## The Story: A Weather App

Imagine a weather app that predicts whether it will rain.

Every day, the app provides:
- A **probability of rain**
- A **final decision** (rain or no rain)

People use this information to decide:
- Whether to carry an umbrella
- Whether to cancel outdoor plans

Now let’s understand how accuracy and calibration judge this app.

---

## Accuracy: Did the App Get It Right?

Accuracy ignores probabilities.

It only checks whether the final decision was correct.

Suppose the app follows this rule:
- If predicted probability ≥ 50% → predict rain
- If predicted probability < 50% → predict no rain

### Accuracy Formula

Accuracy =  
(Number of correct predictions) / (Total number of predictions)

---

### Example

Over 10 days:
- The app predicts rain on 6 days
- It actually rains on 5 of those days
- The app predicts no rain on 4 days
- It does not rain on 3 of those days

Correct predictions = 5 + 3 = 8

Accuracy = 8 / 10 = 80%

Accuracy answers:
> “How often did the app’s final decision match reality?”

It does **not** care whether the app said 51% or 99%.

---

## Calibration: Did the Confidence Mean What It Said?

Calibration looks at probabilities.

It asks:
> “When the app says 80% chance of rain, does it actually rain about 80% of the time?”

To measure this, we group days by predicted probability.

---

### Calibration Formula (Intuition)

For a given predicted probability *p*:

Observed frequency =  
(Number of rainy days when prediction was p)  
/ (Number of days predicted with probability p)

A model is well-calibrated when:

Observed frequency ≈ Predicted probability

---

### Example

Suppose the app says “80% chance of rain” on 10 different days.

- If it rains on 8 of those days → well-calibrated
- If it rains on 4 of those days → poorly calibrated

Calibration answers:
> “Can I trust the confidence number?”

---

## Why Accuracy and Calibration Are Different

Accuracy focuses on **decisions**.  
Calibration focuses on **confidence**.

A model can:
- Make the right decision often
- But exaggerate or understate its confidence

Or:
- Give honest probabilities
- But still make wrong decisions sometimes

---

## Two Weather Apps

### App A: Accurate but Poorly Calibrated

This app usually predicts the correct outcome:
- When it predicts rain, it often rains
- When it predicts no rain, it often stays dry

However:
- On days when it says “90% chance of rain”
- It actually rains only about 60% of the time

App A:
- Has high accuracy
- Has misleading confidence

---

### App B: Well-Calibrated but Less Accurate

This app is cautious with its probabilities.

For example:
- When it says “60% chance of rain”
- It actually rains about 60% of the time

However:
- Its final rain/no-rain decisions are not always correct

App B:
- Has honest confidence
- Has lower accuracy

---

## Key Difference

| Metric | What It Measures |
|------|------------------|
Accuracy | Was the final decision correct? |
Calibration | Did the confidence match reality? |

---

## Memory Hooks

- Accuracy: “Was I right?”
- Calibration: “Was I honest about how sure I was?”
- High confidence does not guarantee reliability
- Probabilities should mean what they say

---

## Final Thought

An accurate model tells you the right answer.

A calibrated model tells you how much to trust that answer.

The best models do both.
