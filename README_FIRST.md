# Final Deep Learning Coursework — how to run

Everything is in **one notebook**:

```
final_deep_learning_coursework.ipynb
```

No local setup, no separate `src/` upload, no moving files between your PC and
Colab. The notebook contains:

- all Python source code,
- the written report,
- the saved figures and metrics,
- a results viewer.

## 1. Open it in Colab

1. Upload the whole folder to Google Drive, or upload just the `.ipynb` file.
2. Right-click the notebook → **Open with → Google Colaboratory**.
3. `Runtime → Change runtime type → T4 GPU` if you want to train.

## 2. Choose a mode

At the top of the notebook, set:

```python
MODE = "view"
```

| Mode | What it does | Time | GPU? |
|---|---|---|---|
| `"view"` | Unpacks the saved results and displays the table, figures, confusion matrices, reports and errors | 1–2 min | No |
| `"quick"` | Downloads data and trains a quick BiLSTM baseline | 5–15 min | Optional |
| `"full"` | Trains BiLSTM, GRU, Word2Vec/FastText, mBERT and AfriBERTa, then evaluates | 2–4 hours | Yes |
| `"crosslingual"` | Runs the optional translation + English BERT extension | 1–2 hours | Yes |

Then `Runtime → Run all`.

## 3. What you get in `"view"` mode

- final model comparison table,
- EDA figures (label histogram, text length, word clouds),
- tokenisation comparison,
- training curves and confusion matrices,
- per-class reports,
- example misclassifications,
- the written report.

Export to PDF with `File → Print → Save as PDF`.

## 4. What is not included

- The **cross-lingual extension** is optional. It is implemented in the notebook
  (`MODE = "crosslingual"`) but the saved results do not include it because it
  needs a GPU and a lot of time.
- The assignment allows **Swahili News OR Twitter sentiment**. This project uses
  Swahili News; Twitter EDA is included as supplementary analysis.

## 5. Submission checklist

- [ ] `report/report.md`
- [ ] this notebook with outputs (or its PDF)
- [ ] `outputs/figures/`
- [ ] `outputs/metrics/`

If a model is missing from the results, do not invent a number. State “not run”.
