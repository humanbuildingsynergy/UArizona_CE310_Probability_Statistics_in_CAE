# CE 310 — Probability and Statistics in Civil and Architectural Engineering

**University of Arizona · Open course materials**

A full-semester applied statistics course for third-year Civil and Architectural
Engineering students. It runs in two halves: seven Excel-based modules covering
descriptive statistics through correlation, then six Python modules in Google
Colab covering regression through bootstrap confidence intervals, closing with a
group capstone on real building-energy data.

Everything here is student-facing and ready to teach or adapt. Answer keys,
grader scripts, and exam instruments are deliberately not included — see
[What is not here](#what-is-not-here).

---

## Course modules

Each module is one week, numbered in teaching order. Files inside a module carry
the same number, so an alphabetical listing is also the order you use them in.

| # | Topic | Tool | Contents |
|---|---|---|---|
| [01](01_descriptive-statistics/) | Descriptive statistics and the flaw of averages | Excel | Lecture, quiz, exercise, assignment, data |
| [02](02_distribution-shape/) | Reading distributions: histograms, skew, and spread | Excel | Lecture, quiz, exercise, assignment |
| [03](03_probability-and-bayes/) | Probability, conditioning, and Bayes' rule | Excel | Lecture, quiz, exercise, assignment, data |
| [04](04_poisson-distribution/) | Poisson and binomial models for rare events | Excel | Lecture, quiz, exercise, assignment, data |
| [05](05_normal-distribution/) | The normal distribution in civil engineering | Excel | Lecture, quiz, exercise, assignment, data |
| [06](06_empirical-percentiles/) | Empirical percentiles and exceedance in practice | Excel | Lecture, quiz, exercise, assignment, data |
| [07](07_correlation/) | Correlation: covariance, Pearson r, and scatter plots | Excel | Lecture, quiz, exercise, assignment |
| [08](08_midterm-review/) | Midterm review and study materials | — | Logistics, review slides, study guide |
| [09](09_simple-regression/) | Simple linear regression — **first Python module** | Python | Lecture, quiz, lab, assignment |
| [10](10_multiple-regression/) | Multiple linear regression | Python | Lecture, quiz, lab, assignment |
| [11](11_hypothesis-testing/) | Hypothesis testing: t-tests and ANOVA | Python | Lecture, quiz, lab, assignment |
| [12](12_sensitivity-analysis/) | Sensitivity analysis and tornado plots | Python | Lecture, quiz, lab, assignment |
| [13](13_monte-carlo/) | Monte Carlo simulation | Python | Lecture, quiz, lab, assignment |
| [14](14_bootstrap-confidence-intervals/) | Bootstrap confidence intervals | Python | Lecture, quiz, lab, assignment |
| [15](15_capstone/) | Group capstone: open-dataset building analysis | Python | Orientation, study guide, lab, client briefs, report instructions, presentation rubric |
| [16](16_capstone-presentations/) | Capstone presentation session | — | Session slides |

> **Tutorials are temporarily withheld.** Each week normally ships a step-by-step
> Excel or Python tutorial carrying the procedures — the lectures teach concepts
> and deliberately avoid syntax. Those tutorials, along with the Week 9 Python
> on-ramp for students new to the language, are being revised and will be added
> back. Until then the labs assume you can supply the procedural steps yourself.

---

## Repository layout

An Excel module and a Python module, side by side:

```
06_empirical-percentiles/            11_hypothesis-testing/
  06.1_lecture.pdf                     11.1_lecture.pdf
  06.2_prelab-quiz.pdf                 11.2_prelab-quiz.pdf
  06.3_in-class-exercise.pdf           11.3_lab.ipynb
  06.4_in-class-worksheet.xlsx         11.4_assignment.pdf
  06.5_assignment.pdf                  11.5_assignment-starter.ipynb
  06.6_assignment-worksheet.xlsx
  data/                              datasets/
                                       CSVs used by several modules
```

Everything is PDF except where the format has to be live: labs and assignment
starters are `.ipynb`, and worksheets are `.xlsx`.

The `.xlsx` files are **blank worksheets, not answers** — labelled cells for
students to type into, which is also what makes the labs auto-gradable.

---

## Using the materials

### Excel modules (1–7)

Open the in-class exercise PDF, open the worksheet `.xlsx`, and load the CSV from
that module's `data/` folder. Any spreadsheet program with `PERCENTILE`,
`COUNTIF`, `SUMPRODUCT`, and `CORREL` will work.

### Python modules (9–15)

The labs are Jupyter notebooks written for Google Colab, so nothing needs
installing. Open [colab.research.google.com](https://colab.research.google.com),
choose **File → Open notebook → GitHub**, and paste this repository's URL.

Each lab that reads a CSV starts with an upload cell:

```python
from google.colab import files
uploaded = files.upload()      # pick the CSV you downloaded from this repo
```

Download the CSV first — from `datasets/` for modules 9–14, or from the module's
own `data/` folder.

---

## Datasets

All datasets are public-domain or derived from public sources (DOE commercial
reference buildings, NOAA climate records).

| File | Used by |
|---|---|
| `datasets/Week5_DOE_MedOffice_ZoneTemp_2023.csv` | Modules 7 and 9–14 |
| `datasets/Week15_*_Dataset.csv` — 5 building types | Module 15 capstone |
| `01_descriptive-statistics/data/Week1_Tucson_Weather_2023.csv` | Module 1 |
| `03_probability-and-bayes/data/Week3_Tucson_Office_Energy_2023.csv` | Module 3 |
| `04_poisson-distribution/data/Week4_Tucson_Precipitation_Daily_2013_2022.csv` | Module 4 |
| `05_normal-distribution/data/Week5_CE_Measurements.csv` | Module 5 |
| `06_empirical-percentiles/data/Week6_Noise_Measurements.csv` | Module 6 |

The five capstone datasets are a no-search-required fallback. Teams are
encouraged to choose their own instead — see the capstone module's dataset
selection guide.

---

## What is not here

Kept in a private instructor repository so the assessments stay usable:

- answer keys and expected values
- auto-grader scripts, grading rubrics, and preceptor guides
- the midterm concept exam and practicum, and the final written exam
- instructor editions of the pre-lab quizzes

Instructors at other institutions are welcome to request them — open an issue or
contact the author. Please do not post keys or graders back to this repository.

---

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — use, adapt, and
redistribute freely, including commercially, with attribution. See [LICENSE](LICENSE).

## Citation

> Jung, W. (2026). *CE 310: Probability and Statistics in Civil and Architectural
> Engineering* [Open course materials]. University of Arizona.
> https://github.com/humanbuildingsynergy/UArizona_CE310_Probability_Statistics_in_CAE

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
