# Seunghyun Yeo

**Data Analytics · NLP · Applied AI · Evidence-based Policy**  
The Chinese University of Hong Kong (CUHK) — BSSc in Data Science & Policy Studies, Minor in Computer Science (2026)  
Exploring early-career data analysis, research and applied AI opportunities in **South Korea and Hong Kong**.

I work across survey data, natural-language processing and practical ML experiments. Below, **team experiment results** are distinguished from **my direct code or analytical work**.

## Selected work

### 1. CUHK Capstone — Curriculum–Market Alignment in Data Science Education (2025–2026)
- **Team study:** collected an archive of **5,525** Hong Kong job advertisements, with **2,074 usable job ads** in the final analysis, and aligned skills to **91 course descriptions**.
- **Approach:** job-ad section extraction, SkillNER, course-to-skill mapping, demand-weighted coverage and Streamlit visualization.
- **Recorded results:** demand-weighted **Top-20 coverage of 39.14% (DSPS) vs 35.95% (CDAS)**. These are text-skill alignment measures, *not* employment rates or measures of education quality.
- The submitted capstone report is complete; public code/data reproduction is still pending. [Metrics, methodological cautions and portfolio plan](PROJECT_EVIDENCE.md#1-cuhk-capstone--curriculummarket-alignment-in-data-science-education-20252026)

### 2. [FeelLog — Multimodal Emotion Journaling AI](https://github.com/StaG-lab/AI_Dev_3rd_Project) (2025)
- **Team evaluation:** audited **40,550** emotion-labeled images and identified **12,176** cases in which uploader labels disagreed with annotator-majority labels.
- **Team model results:** EmoNet validation accuracy **75.20% → 88.12%** following dataset/label rework; later checkpoint **macro F1 0.8097**. The change is *not* attributable to architecture alone.
- **My implementation:** [PyTorch CUDA/AMP/TF32 training loop](https://github.com/StaG-lab/AI_Dev_3rd_Project/blob/main/YEO/core/training/trainer_v3.py), classification metrics, and a [Gemini period-query and summary prototype](https://github.com/StaG-lab/AI_Dev_3rd_Project/pull/37) separate from the released team application. A [GPU experiment log](https://github.com/StaG-lab/AI_Dev_3rd_Project/blob/main/YEO/train_speedup_emonet_v2.ipynb) records **86,974 training samples / 1 epoch / 10m 27s**; **no controlled speedup percentage has been established**.
- [Team checkpoint JSON](https://github.com/StaG-lab/AI_Dev_3rd_Project/blob/main/CHOI/feellog-project_03/reports/model/emonet_50_2_percent_trained_1_metrics.json) · [Model experimentation PR](https://github.com/StaG-lab/AI_Dev_3rd_Project/pull/13)

### 3. PHQ-9 Risk Classification — 2024 Korean Community Health Survey (2025)
- **Team study:** approximately **231,206** analyzed survey records; preprocessing, feature engineering, and comparison of CatBoost, XGBoost, logistic regression and ensemble classifiers.
- **Recorded team result:** threshold-adjusted soft-voting classifier, **positive-class recall 0.750**, **macro F1 0.694**, **ROC AUC 0.8418** (internal experiment).
- This is a survey-based risk classification research prototype, **not a validated diagnostic tool**. Source: internal team model/preprocessing reports; code and full results are not currently published.

### 4. HKCSS — Social Impact Assessment Internship (2022)
- **My reported work:** cleaned **200+** multilingual social-inclusion survey responses, including multiple-choice recoding and free-text classification.
- Prepared Python frequency summaries and visualizations for **100+ T0/T1 respondents**, conducted a paired pre/post test, and supported demographic research and inclusion-indicator data-feasibility checks.
- The pre/post test in my archived presentation did **not** establish a statistically significant change. Respondent data and internal research materials remain private.

## Additional projects and software work

| Project | My traceable contribution |
|---|---|
| [US NHANES Survey EDA](https://github.com/jeongmin-C/Group-3/blob/develop/view.ipynb) | XPT merging, PHQ-9 data checking, exploratory plots/correlations; [merged PR #9](https://github.com/jeongmin-C/Group-3/pull/9). **Different dataset from the Korean study above.** |
| [CSCI2720 — Hong Kong Events & Venues](https://github.com/Jonathanc1002/CSCI2720project) | LCSD XML ingestion, Express controllers and demo backend functionality: [ingestion](https://github.com/Jonathanc1002/CSCI2720project/commit/b0257b9fd31a0ed042417d17b5e4a8459316019e), [controllers](https://github.com/Jonathanc1002/CSCI2720project/commit/260478008a9e47f17cd8e74d8f8b2dba4af7f553), [favorites](https://github.com/Jonathanc1002/CSCI2720project/commit/8331ca3aadee72cb29322cfbf14273eedda1309a). |
| [CSCI3100 — AI-assisted Code Annotation](https://github.com/dvex3/csci-3100-project) | Python AST parsing, **seven committed parser test functions**, Azure OpenAI prompt updates: [parser](https://github.com/dvex3/csci-3100-project/pull/4), [tests](https://github.com/dvex3/csci-3100-project/pull/6), [prompts](https://github.com/dvex3/csci-3100-project/pull/10). |

## Technical skills

**Python**, pandas, NumPy, scikit-learn, PyTorch, SQL, NLP / skill extraction, survey statistics, exploratory analysis, ML evaluation, Streamlit, Git/GitHub, pytest; familiarity with JavaScript, Express and MongoDB.

## Evidence and portfolio development

**[Project Evidence Register](PROJECT_EVIDENCE.md)** — verified figures, my contributions vs team results, links to source code, unresolved validation tasks and a checklist for later portfolio case studies.

Evidence quality takes precedence over inflated claims. Restricted survey responses, protected research data, raw job advertisements and confidential assets are not uploaded to this profile.
