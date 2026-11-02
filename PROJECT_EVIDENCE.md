# Project Evidence Register

Last reviewed: **2026-11-03 (KST)**. This register is the source-of-truth checklist for updating my résumé, GitHub profile and future portfolio. It separates **individual work**, **team results** and **unverified claims**.

## Evidence rules

- **[Individual]** means my own written report, code, commit or PR explicitly supports my contribution.
- **[Team]** means a shared project report/experiment; it must not be described as my sole achievement.
- **[Recorded]** means the number exists in a submitted report, notebook output or metric file. It does *not* necessarily mean a fully reproduced experiment.
- **[Pending]** means verification/reproduction is required before stronger claims are made.
- Percentage **points (pp)** are different from relative percentages; neither implies causation.
- Public documents contain only aggregate, non-identifying results. No raw HKCSS respondent data, restricted job-posting corpora, sensitive videos, licensed survey microdata or private contact information should be uploaded.

---

## 1. CUHK Capstone — Curriculum–Market Alignment in Data Science Education (2025–2026)

**Problem:** Examine whether CUHK data-science-related course descriptions explicitly cover skills in Hong Kong data-related job advertisements.

**Pipeline:** job-ad collection / section extraction / deduplication → SkillNER and standardized skills → weighted curriculum–labor-market alignment → Streamlit exploration.

### Documented quantitative facts [Team; Recorded]

| Metric | Value | Interpretation |
|---|---:|---|
| Original scraped/collected job advertisements | **5,525** | Raw acquisition archive; *not* final analyzed ads |
| High-confidence unique job advertisements | **3,080** | Strict-deduplication count |
| Working job-ad corpus | **3,109** | Working corpus with a different inclusion rule; don't present as subsequent to 3,080 |
| Job advertisements with usable sections | **2,074** | 66.7% of working corpus |
| Distinct course texts analyzed | **91** | DSPS 23 + CDAS 68 |
| DSPS demand-weighted Top-20 skill coverage | **39.1408%** | Text-based skills metric |
| CDAS demand-weighted Top-20 skill coverage | **35.95%** | Text-based skills metric |
| Program difference on this metric | **~3.19 pp** | Descriptive comparison, not a superiority or employability claim |

**Sources:** personal final submitted report, `1155149594_YeoSeunghyun_Capstone_FinalReport_DSPS4802.docx` (May 11, 2026), methodology summary and results tables. Public code/data reproducibility audit is still pending. The previously published **2,037** job descriptions and **1,322** skill features describe an *earlier stage* in the work; do not silently merge those numbers with the final-report counts.

**Resume-safe formulation:** “Analyzed 2,074 usable job advertisements from an archive of 5,525 and mapped 91 course texts to standardized skills; compared demand-weighted Top-20 coverage (DSPS 39.14%, CDAS 35.95%) in a CUHK capstone team study.”

**To verify before the portfolio:** confirm the local code revision used for the submitted table, reproducible post-cleaning counts, Streamlit screenshot/commit, per-program course list and ownership of each pipeline component.

---

## 2. FeelLog — Multimodal emotion journaling AI (ESTsoft WASSUP AI, 2025)

**Problem:** Analyze a short video diary using facial imagery, speech and text to create emotion summaries.

### Data quality and model evaluation [Team; Recorded]

| Metric | Value | Interpretation |
|---|---:|---|
| Labeled images audited in the 10% sample | **40,550** | Data-quality audit set |
| Uploader label vs annotator-majority disagreement | **12,176 (30.0%)** | Separate label-conflict definition; overlaps with other agreement categories |
| Images with full annotator agreement | **20,535 (50.6%)** | The agreement categories need not equal the uploader-conflict metric |
| Emotion classes | **7** | Joy, embarrassment, anger, anxiety, hurt, sadness, neutral |
| Earlier EmoNet 50%-sample validation accuracy | **75.20%** | Earlier preprocessing/data setup |
| Later EmoNet validation accuracy | **88.12%** | After label/data rework and person-aware split |
| Accuracy change | **+12.92 pp** | **Not** attributable solely to architecture, CUDA or any one intervention |
| Later EmoNet macro F1 | **0.8097** | From the checkpoint paired with 88.12% validation accuracy |
| Another checkpoint macro F1 | **0.8109** | Different checkpoint (88.00% validation accuracy) |

**Public model result:** [EmoNet checkpoint metrics JSON](https://github.com/StaG-lab/AI_Dev_3rd_Project/blob/main/CHOI/feellog-project_03/reports/model/emonet_50_2_percent_trained_1_metrics.json).
**Internal report:** “이미지 모델 분석 결과 보고서” on the team's connected Google Drive/Notion. Findings are **team outcomes**; my own contribution is evidenced by the `YEO/` directory, submitted notebooks, pull requests and prototype work.

### My implementation evidence [Individual; Recorded]

- [CUDA/AMP/TF32-capable PyTorch training loop](https://github.com/StaG-lab/AI_Dev_3rd_Project/blob/main/YEO/core/training/trainer_v3.py): mixed precision (autocast/GradScaler), early stopping, optional checkpoint saving, class F1 and confusion-matrix reporting.
- [Single-epoch EmoNet GPU run](https://github.com/StaG-lab/AI_Dev_3rd_Project/blob/main/YEO/train_speedup_emonet_v2.ipynb): **86,974** training samples, batch size **64**, **10m 27s** for one epoch, validation accuracy **79.06%** in *that run*. This is **not** the final team's 88.12% model.
- [Period-query/Gemini prototype PR](https://github.com/StaG-lab/AI_Dev_3rd_Project/pull/37): prototype of period intent parsing, aggregation and summary; separate from the final team app.
- [Model experimentation PR](https://github.com/StaG-lab/AI_Dev_3rd_Project/pull/13).

**[Not measured]** The estimates of **10–30% cuDNN/TF32 speed gain**, **20–40% AMP speed gain** and memory reduction in `YEO/v2_summary.md` are **expected effects**, *not benchmarked personal before/after results*. Do not put these values in a résumé.

**To verify before the portfolio:** run a controlled identical-model/data/GPU benchmark (AMP/TF32 on/off), capture samples/sec, epoch duration and peak VRAM; trace my specific model/data-quality contributions through PRs and experiment reports; evaluate a held-out subject-independent test set. Do not publish emotion image samples without redistribution permission.

---

## 3. Hong Kong Council of Social Service (HKCSS) — Social Impact Assessment internship (2022)

### My documented tasks [Individual; Recorded]

- Personally cleaned **200+** multilingual Project PRAISE social-inclusion survey responses (coded variables, multi-select dummy variables, free-text classification, invalid-response rules).
- Analyzed a separate **100+ respondent** Tung Chung T0/T1 survey using Python for ethnicity-breakdown frequency tables, visualizations and Likert-scale scores.
- Conducted a **paired t-test** on pre/post sense-of-community responses; the internship presentation reported **no statistically significant change**. Do not imply the intervention improved outcomes.
- Supported population/demographic background research, indicator data-feasibility checking, questionnaire wording and documentation, and expert-meeting minutes.
- Personal final reflection reports **320 hours** of internship work. The submitted report and presentation differ on the exact final work date (Aug 8 vs Aug 26); use official certification to resolve the dates.

**Corroborating archive, not a statement of my exact cleaned sample:** saved Yuen Long survey response sheets contained **100 English responses** and **133 Chinese responses** at review time. These **233 raw archived rows** should **not** automatically replace my report's “200+ personally cleaned” figure or be attributed solely to me.

**Sources (internal; never publish respondent-level materials):** `1155149594_DSPS3801_Report.docx`, `Internship sharing`, and Project PRAISE survey response sheets on connected Drive.

**Resume-safe formulation:** “Cleaned 200+ multilingual social-inclusion survey records; prepared Python frequency tables, comparisons and a paired t-test for 100+ T0/T1 survey respondents; supported policy-indicator feasibility research.”

**To verify before the portfolio:** retrieve only aggregated, disclosure-safe tables and transformation examples; independently count final cleaned files if authorized. Replace any confidential row-level examples with synthetic data.

---

## 4. PHQ-9 risk classification — 2024 Korean Community Health Survey (ESTsoft WASSUP AI, 2025)

**Do not confuse this project with the earlier US NHANES EDA.** They have different data and outcomes.

### Team report results [Team; Recorded]

| Metric | Value |
|---|---:|
| Final cleaned/merged analysis records | **231,206** |
| Data source | **2024 Community Health Survey (Korea)** |
| Target | PHQ-9 total score **≥5** (study-defined risk category) |
| Final selected method | Soft Voting ensemble; risk-recall-oriented decision threshold |
| Voting decision threshold | **0.2837** |
| Positive-class recall | **0.750** |
| Macro F1 | **0.694** |
| Accuracy | **0.773** |
| ROC AUC | **0.8418** |

**Source:** team's “3조_모델 분석 보고서.pdf” and “3조_전처리 보고서.pdf” on connected Drive; not independently rerun. Model comparisons included XGBoost, CatBoost, logistic regression, stacking and threshold tuning.

**Important:** This is retrospective internal validation, **not** a clinically validated diagnostic system or proof of real-world intervention. Before publishing claims, verify leakage-free feature sets (especially PHQ-9 questions), the train/validation split, weighting/class-imbalance decisions and cohort provenance.

**Resume-safe formulation:** “Participated in analysis of 231,206 Korean Community Health Survey records and a PHQ-9 risk classification team project; the final soft-voting configuration recorded recall 0.750 and macro F1 0.694 (internal evaluation).”

---

## 5. NHANES Survey EDA (US; separate exploratory project, 2025)

- [My team notebook](https://github.com/jeongmin-C/Group-3/blob/develop/view.ipynb) and [merged PR #9](https://github.com/jeongmin-C/Group-3/pull/9).
- [Individual contribution] Merge XPT data, inspect missingness, process PHQ-9 responses and explore distributions/correlations.
- **No verified improvement percentages**. Keep as an auxiliary project rather than claiming outcomes from the Korean survey.

## 6. Additional software engineering evidence

- [CSCI2720 events/venues backend](https://github.com/Jonathanc1002/CSCI2720project): data ingestion, Express controllers/routes, venue/comment/favorites features; committed changes linked in profile README.
- [CSCI3100 code-annotation project](https://github.com/dvex3/csci-3100-project): Python AST parsing, **seven committed parser test functions**, Azure OpenAI prompt changes. CI pass rate unverified.

---

## Resume/GitHub/portfolio synchronization checklist

| Project | Resume positioning | GitHub evidence | Future portfolio artifact |
|---|---|---|---|
| CUHK capstone | Job data + NLP + 91 courses + coverage | Literature/results register until code reproduced | Pipeline architecture, limitations and two-program skill coverage figure |
| FeelLog | Data labeling quality + experiment improvement + personal GPU work | Team metrics JSON, `YEO/` code, PRs | Experiment matrix, confusion-matrix narrative, controlled runtime benchmark |
| HKCSS | 200+ cleaned, 100+ T0/T1 + statistical analysis | **Aggregates only**; private documents stay private | Synthetic before/after data-cleaning example + safe statistical memo |
| Korean CHS | 231,206 + recall/F1 (team model) | Method/results register (code only if publishable) | Threshold tradeoff chart, class balance, leakage audit |
| NHANES | Optional / not in 1-page résumé | Notebook + merged PR | Short EDA case study |

### Before every future revision

1. Check that every number has an explicit **dataset, split, metric, method, and source**.
2. Label team outcomes as team outcomes; keep personal commits/outputs separate.
3. Never use estimated GPU speedup as measured performance.
4. Avoid using "accuracy" to describe class-wise proportions, Top-K coverage or survey intervention impacts.
5. Keep an external-facing 1-page Korean résumé concise; reserve extended methodology, caveats and secondary projects for the portfolio.
