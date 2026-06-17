# 201-TakeMeter

## Community Choice and Reasoning

### Selected Community

Describe the online community or dataset domain you selected.

### Reasoning

Explain why this community was chosen and why it is suitable for a text classification task. Discuss the relevance of the labels and any interesting characteristics of the community.

---

## Label Taxonomy

### Label Definitions

| Label   | Definition  |
| ------- | ----------- |
| Label 1 | Description |
| Label 2 | Description |
| Label 3 | Description |

### Example Posts for Each Label

#### Label 1

* Example 1: ...
* Example 2: ...

#### Label 2

* Example 1: ...
* Example 2: ...

#### Label 3

* Example 1: ...
* Example 2: ...

---

## Dataset Creation

### Data Collection Source

Describe where the posts were collected from and any filtering criteria used.

### Labeling Process

1. How labels were assigned.
2. Any annotation guidelines followed.
3. Any quality checks performed.

### Label Distribution

| Label   | Count | Percentage |
| ------- | ----- | ---------- |
| Label 1 | X     | X%         |
| Label 2 | X     | X%         |
| Label 3 | X     | X%         |

### Difficult-to-Label Examples

#### Example 1

**Post**

> "..."

**Decision:** Label X

**Reasoning:** Explain why.

#### Example 2

**Post**

> "..."

**Decision:** Label Y

**Reasoning:** Explain why.

#### Example 3

**Post**

> "..."

**Decision:** Label Z

**Reasoning:** Explain why.

---

## Fine-Tuning Approach

### Base Model

Specify the model used for fine-tuning.

### Training Setup

* Training/validation split
* Number of epochs
* Batch size
* Learning rate
* Any preprocessing steps

### Hyperparameter Decision

Discuss at least one important hyperparameter choice and why it was selected.

Example:

> I chose a learning rate of 2e-5 because higher values caused unstable validation loss during preliminary experiments.

---

## Zero-Shot Baseline

### Prompt Used

```text
Classify the following post into one of: Label A, Label B, Label C.

Post:
{post_text}

Return only the label.
```

### Evaluation Procedure

Describe:

* How predictions were collected
* Number of examples evaluated
* Any automation used

---

## Evaluation Results

### Overall Metrics

| Model              | Accuracy |
| ------------------ | -------- |
| Zero-Shot Baseline | X.XX     |
| Fine-Tuned Model   | X.XX     |

### Per-Class Metrics

| Label   | Precision | Recall | F1 |
| ------- | --------- | ------ | -- |
| Label 1 |           |        |    |
| Label 2 |           |        |    |
| Label 3 |           |        |    |

### Confusion Matrix

| Actual \ Predicted | Label 1 | Label 2 | Label 3 |
| ------------------ | ------- | ------- | ------- |
| Label 1            |         |         |         |
| Label 2            |         |         |         |
| Label 3            |         |         |         |

### Error Analysis

#### Incorrect Prediction 1

* **Actual Label:**
* **Predicted Label:**
* **Post:**
* **Analysis:**

#### Incorrect Prediction 2

* **Actual Label:**
* **Predicted Label:**
* **Post:**
* **Analysis:**

#### Incorrect Prediction 3

* **Actual Label:**
* **Predicted Label:**
* **Post:**
* **Analysis:**

### Sample Classifications

| Post      | Predicted Label | Confidence | Correct? |
| --------- | --------------- | ---------- | -------- |
| Example 1 |                 |            |          |
| Example 2 |                 |            |          |
| Example 3 |                 |            |          |
| Example 4 |                 |            |          |
| Example 5 |                 |            |          |

#### Correct Example Explanation

Choose one correctly classified example and explain why the model's prediction was appropriate.

---

## Reflection

### What the Model Learned

Discuss patterns the model appears to have captured successfully.

### What You Intended

Compare the learned behavior to your original labeling goals.

### Surprises

Describe any unexpected successes or failures.

---

## Specification Reflection

### How the Specification Helped

Describe one way the project specification improved your implementation process.

### Divergence from the Specification

Explain one way your implementation differed from the original specification and why that change was made.

---

## AI Usage Disclosure

### AI Assistance Instance #1

**Task:** Describe what you asked the AI to do.

**Output Used:** Explain what was incorporated.

**Your Revisions:** Describe modifications or corrections you made.

### AI Assistance Instance #2

**Task:** Describe what you asked the AI to do.

**Output Used:** Explain what was incorporated.

**Your Revisions:** Describe modifications or corrections you made.

### Annotation Assistance Disclosure

State whether AI was used during data annotation or labeling. If used, describe exactly how it assisted and how final labeling decisions were verified.

---

## Conclusion

Summarize:

* Dataset quality
* Fine-tuning results
* Comparison against the zero-shot baseline
* Key lessons learned
