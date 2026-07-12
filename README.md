# Computational and AI Methods in Climate Economics
*(CEMRACS 2026 Summer School — "Modeling and AI for Environmental Transition", July 14–15, 2026)*

This mini-course introduces **computational and AI methods for climate
economics** to the participants of the
[CEMRACS 2026](https://cemracs2026.math.cnrs.fr/en/) summer school. Over three
lectures it builds a modern deep-learning toolkit for solving, estimating, and
performing uncertainty quantification on high-dimensional dynamic economic
models — with a running application to climate–economy integrated assessment
models (IAMs) and optimal carbon taxation.

The course is delivered as **three lectures** (Parts I–III) paired with two
hands-on **practical sessions** taught by Maria Pia Lombardo.

> **Companion textbook treatment.** This mini-course is a focused, climate-economics-oriented
> excerpt of a much broader body of material. For a thorough, textbook-style
> treatment of deep learning for **solving and estimating dynamic economic and
> financial models** — with full lecture notes, slides, and runnable code — see the
> companion repository
> [**Deep Learning for Solving and Estimating Dynamic Economic Models**](https://github.com/sischei/Deep_Learning_for_Solving_And_Estimating_Dynamic_Economic_Models).

## Quick Links

- [Quick Start](#quick-start)
- [Detailed Timetable](#detailed-timetable)
- [Course Overview](#course-overview)
- [Materials by Lecture](#materials-by-lecture)
- [References](#references)
- [Citation](#citation)
- [Lecturer](#lecturer)

## Quick Start

### Prerequisites

- Basic economics and econometrics
- Familiarity with Python programming (please look at this
  [Python refresher](python_refresher), or at the more comprehensive course on
  [QuantEcon Python Programming](https://python-programming.quantecon.org/intro.html))
- Solid understanding of basic calculus and probability (see
  [Mathematics for Machine Learning](https://mml-book.github.io/))

### Local Setup

All notebooks run on **Python 3.10+**. The main dependencies are:

| Package | Purpose |
|---------|---------|
| [NumPy](https://numpy.org/) | Numerical computing |
| [SciPy](https://scipy.org/) | Scientific computing |
| [Pandas](https://pandas.pydata.org/) | Data analysis |
| [Matplotlib](https://matplotlib.org/) | Visualization |
| [scikit-learn](https://scikit-learn.org/) | Classical machine learning & Gaussian processes |
| [TensorFlow](https://www.tensorflow.org/) >= 2.15 | Deep learning (DEQNs, surrogates) |
| [TensorFlow Probability](https://www.tensorflow.org/probability) | Gaussian processes & deep UQ |
| [TensorBoard](https://www.tensorflow.org/tensorboard) | Training monitoring |
| [PyTorch](https://pytorch.org/) >= 2.0 | Deep learning (selected notebooks, optional) |

To install all dependencies at once:

```bash
pip install -r requirements.txt
```

> **Note:** a `requirements.txt` will be added to the repository root before the
> course begins. Until then, install the packages listed above directly.

### Course Platform

- Lecture materials (slides, code, readings) will be made available via this
  [GitHub repository](https://github.com/sischei/cemracs2026_DEQN) and on
  **Nuvolos Cloud**.
- To enroll in this class, please click on the enrollment key
  [`ENROLLMENT_KEY_TBA`](https://app.nuvolos.cloud/) and follow the steps.
  *(The enrollment key will be circulated before the first lecture.)*
- All required software and dependencies are pre-installed on the platform.
- Nuvolos support: <support@nuvolos.cloud>

On the [Nuvolos Cloud](https://nuvolos.cloud/) platform used during the course,
all dependencies are pre-installed. The `requirements.txt` file is provided for
participants who wish to run the notebooks on their own machines.

## Detailed Timetable

### Lecture 1 (Part I) — Tuesday, July 14th (16:00–17:30)
**Deep Equilibrium Nets**

| Time | Topic | Materials |
|------|-------|-----------|
| 16:00 – 17:30 | Introduction to Deep Equilibrium Nets (DEQNs): solving dynamic stochastic economic models by approximating equilibrium functions with neural networks and minimizing equilibrium (Euler) residuals | Slides: [`01_DeepEquilibriumNets`](lectures/lecture_1/slides/01_DeepEquilibriumNets.pdf)<br>Notebooks: [`01_Brock_Mirman_1972_DEQN`](lectures/lecture_1/code/01_Brock_Mirman_1972_DEQN.ipynb), [`02_Brock_Mirman_Uncertainty_DEQN`](lectures/lecture_1/code/02_Brock_Mirman_Uncertainty_DEQN.ipynb)<br>Extended materials: NAS & loss normalization (see [Materials by Lecture](#lecture-1--deep-equilibrium-nets)) |

#### Practical Session 1 — Tuesday, July 14th (17:30–19:00)
**Hands-on DEQN** *(Maria Pia Lombardo)* — guided implementation and exercises building on Lecture 1. Materials: exercise notebooks [`03_DEQN_Exercises_Blanks`](lectures/lecture_1/code/03_DEQN_Exercises_Blanks.ipynb) / [`04_DEQN_Exercises_Solutions`](lectures/lecture_1/code/04_DEQN_Exercises_Solutions.ipynb), plus [`05_StochasticBM_LossComparison`](lectures/lecture_1/code/05_StochasticBM_LossComparison.ipynb) and the extended NAS/loss notebooks in [`lectures/lecture_1/code/`](lectures/lecture_1/code/)

### Lecture 2 (Part II) — Wednesday, July 15th (11:00–12:30)
**Solving the DICE Model with DEQN, and Surrogate Methods**

| Time | Topic | Materials |
|------|-------|-----------|
| 11:00 – 12:30 | Solving the DICE integrated assessment model with DEQNs; surrogate models and Gaussian process regression (GPR) for high-dimensional dynamic programming and estimation | Slides: [`02_DICE_and_Surrogates`](lectures/lecture_2/slides/02_DICE_and_Surrogates.pdf)<br>Notebooks: [`01_DICE_DEQN`](lectures/lecture_2/code/01_DICE_DEQN.ipynb), [`02_GP_Regression`](lectures/lecture_2/code/02_GP_Regression.ipynb), [`03_Surrogate_Models`](lectures/lecture_2/code/03_Surrogate_Models.ipynb) |

### Lecture 3 (Part III) — Wednesday, July 15th (16:00–17:30)
**Deep Uncertainty Quantification and Optimal Taxation**

| Time | Topic | Materials |
|------|-------|-----------|
| 16:00 – 17:30 | Deep uncertainty quantification (Deep UQ) for stochastic IAMs; computing constrained optimal carbon tax rules with deep surrogates | Slides: [`03_DeepUQ_and_Optimal_Taxation`](lectures/lecture_3/slides/03_DeepUQ_and_Optimal_Taxation.pdf)<br>Notebooks: [`01_Deep_UQ`](lectures/lecture_3/code/01_Deep_UQ.ipynb), [`02_Optimal_Carbon_Tax`](lectures/lecture_3/code/02_Optimal_Carbon_Tax.ipynb) |

#### Practical Session 2 — Wednesday, July 15th (17:30–19:00)
**Hands-on DICE / Surrogates / UQ** *(Maria Pia Lombardo)* — guided exercises building on Lectures 2 and 3. Materials: [`lectures/lecture_2/code/`](lectures/lecture_2/code/), [`lectures/lecture_3/code/`](lectures/lecture_3/code/)

## Course Overview

### Scope

This course introduces advancements in machine learning and computational
science to solve, estimate, and quantify uncertainty in dynamic stochastic
economic models, with a focus on climate economics. It covers:

- Deep Equilibrium Nets (DEQNs) for dynamic stochastic models
- The DICE integrated assessment model, solved globally with DEQNs
- Gaussian Process Regression (GPR) and deep surrogate models
- Deep Uncertainty Quantification (Deep UQ) for stochastic IAMs
- Constrained optimal carbon taxation via deep surrogates

### Lecture Progression

**Lecture 1** builds the core method: Deep Equilibrium Nets, a global solution
technique that represents equilibrium policy functions with neural networks and
trains them to minimize equilibrium-condition (Euler) residuals.

**Lecture 2** applies DEQNs to the climate–economy problem — solving the DICE
integrated assessment model — and introduces surrogate methods (Gaussian
process regression and deep surrogates) for high-dimensional dynamic
programming and structural estimation.

**Lecture 3** closes with the estimation-and-uncertainty layer: deep
uncertainty quantification for stochastic IAMs and the computation of
constrained optimal carbon tax rules with deep surrogates.

### Teaching Format

The lectures combine theoretical discussions with hands-on coding exercises in
Python, using [Python](http://www.python.org/),
[scikit-learn](https://scikit-learn.org/),
[TensorFlow](https://www.tensorflow.org/), and
[TensorFlow Probability](https://www.tensorflow.org/probability) so participants
can implement and experiment with the introduced methods directly. Each lecture
is complemented by a **practical session** (taught by Maria Pia Lombardo) in
which participants implement and extend the methods themselves.

## Materials by Lecture

> The tables below list the expected slides, notebooks, and readings for each
> lecture. Individual files are added to the repository as the course
> materials are finalized.

### Lecture 1 — Deep Equilibrium Nets

#### Slides

| # | Slide Deck | Topic |
|---|------------|-------|
| 01 | [`01_DeepEquilibriumNets`](lectures/lecture_1/slides/01_DeepEquilibriumNets.pdf) | Deep Equilibrium Nets (DEQNs) |

#### Notebooks

| # | Notebook | Topic |
|---|----------|-------|
| 01 | [`01_Brock_Mirman_1972_DEQN`](lectures/lecture_1/code/01_Brock_Mirman_1972_DEQN.ipynb) | DEQN: deterministic Brock-Mirman (1972) growth model, exogenous state sampling |
| 02 | [`02_Brock_Mirman_Uncertainty_DEQN`](lectures/lecture_1/code/02_Brock_Mirman_Uncertainty_DEQN.ipynb) | DEQN: stochastic Brock-Mirman with AR(1) TFP uncertainty, Gauss-Hermite quadrature, simulated-path sampling |
| 03 | [`03_DEQN_Exercises_Blanks`](lectures/lecture_1/code/03_DEQN_Exercises_Blanks.ipynb) | **Exercise (blanks):** stochastic BM, endogenous labor, occasionally binding constraints (KKT + Fischer-Burmeister), a small OLG model |
| 04 | [`04_DEQN_Exercises_Solutions`](lectures/lecture_1/code/04_DEQN_Exercises_Solutions.ipynb) | **Exercise (solutions)** for notebook 03 |
| 05 | [`05_StochasticBM_LossComparison`](lectures/lecture_1/code/05_StochasticBM_LossComparison.ipynb) | Loss-kernel comparison (MSE / MAE / Huber / pinball / CVaR / LogCosh) on stochastic Brock-Mirman |

#### Extended / Auxiliary Materials

Optional self-study materials on hyperparameter/architecture search and
multi-objective loss balancing for DEQN training — not required for the core
lecture.

| # | Slide Deck | Topic |
|---|------------|-------|
| 02 | [`02_Neural_Architecture_Search`](lectures/lecture_1/slides/02_Neural_Architecture_Search.pdf) | Neural Architecture Search: random search and Hyperband for DEQN architectures |
| 03 | [`03_Loss_Normalization`](lectures/lecture_1/slides/03_Loss_Normalization.pdf) | Loss normalization: ReLoBRaLo and gradient-conflict mitigation in multi-equation residual losses |

| # | Notebook | Topic |
|---|----------|-------|
| 06 | [`06_NAS_Random_Search_10D`](lectures/lecture_1/code/06_NAS_Random_Search_10D.ipynb) | Random-search NAS on a 10-D regression |
| 07 | [`07_NAS_RandomSearch_Hyperband`](lectures/lecture_1/code/07_NAS_RandomSearch_Hyperband.ipynb) | Random search and successive halving (Hyperband) implemented from scratch |
| 08 | [`08_Loss_Normalization`](lectures/lecture_1/code/08_Loss_Normalization.ipynb) | Multi-component loss balancing (ReLoBRaLo) |

#### Readings

| Reading | Description |
|---------|-------------|
| [`Azinovic_Gaegauf_Scheidegger_2022_DEQN.pdf`](lectures/lecture_1/readings/Azinovic_Gaegauf_Scheidegger_2022_DEQN.pdf) | Azinovic, Gaegauf & Scheidegger (2022). Deep Equilibrium Nets. *International Economic Review* 63(4), 1471-1525 |

### Lecture 2 — DICE with DEQN, and Surrogate Methods

#### Slides

| # | Slide Deck | Topic |
|---|------------|-------|
| 02 | [`02_DICE_and_Surrogates`](lectures/lecture_2/slides/02_DICE_and_Surrogates.pdf) | Solving DICE with DEQNs; Gaussian processes and deep surrogate models |

#### Notebooks

| # | Notebook | Topic |
|---|----------|-------|
| 01 | [`01_DICE_DEQN`](lectures/lecture_2/code/01_DICE_DEQN.ipynb) | Solving the DICE integrated assessment model with DEQNs |
| 02 | [`02_GP_Regression`](lectures/lecture_2/code/02_GP_Regression.ipynb) | Gaussian Process Regression for function approximation |
| 03 | [`03_Surrogate_Models`](lectures/lecture_2/code/03_Surrogate_Models.ipynb) | Deep surrogate models for dynamic programming and estimation |

#### Readings

| Reading | Description |
|---------|-------------|
| [`CDICE_Restud_production.pdf`](lectures/lecture_2/readings/CDICE_Restud_production.pdf) | Folini, Friedl, Kuebler & Scheidegger (2024). The Climate in Climate Economics. *Review of Economic Studies* |
| [`ML_HighDim_JCS.pdf`](lectures/lecture_2/readings/ML_HighDim_JCS.pdf) | Scheidegger & Bilionis (2019). Machine Learning for High-Dimensional Dynamic Stochastic Economies. *Journal of Computational Science* 33, 68-82 |
| [`DeepSurrogates_JFE.pdf`](lectures/lecture_2/readings/DeepSurrogates_JFE.pdf) | Chen, Didisheim & Scheidegger (2026). Deep Surrogates for Finance: With an Application to Option Pricing. *Journal of Financial Economics* |

### Lecture 3 — Deep Uncertainty Quantification and Optimal Taxation

#### Slides

| # | Slide Deck | Topic |
|---|------------|-------|
| 03 | [`03_DeepUQ_and_Optimal_Taxation`](lectures/lecture_3/slides/03_DeepUQ_and_Optimal_Taxation.pdf) | Deep UQ for stochastic IAMs and constrained optimal carbon taxation |

#### Notebooks

| # | Notebook | Topic |
|---|----------|-------|
| 01 | [`01_Deep_UQ`](lectures/lecture_3/code/01_Deep_UQ.ipynb) | Deep uncertainty quantification for stochastic integrated assessment models |
| 02 | [`02_Optimal_Carbon_Tax`](lectures/lecture_3/code/02_Optimal_Carbon_Tax.ipynb) | Constrained optimal carbon tax rules via deep surrogates |

#### Readings

| Reading | Description |
|---------|-------------|
| [`DeepUQ_with_an_application_to_IAM.pdf`](lectures/lecture_3/readings/DeepUQ_with_an_application_to_IAM.pdf) | Friedl, Kuebler, Scheidegger & Usui (2023). Deep Uncertainty Quantification: With an Application to Integrated Assessment Models |
| [`JPE_Macro.pdf`](lectures/lecture_3/readings/JPE_Macro.pdf) | Kuebler, Scheidegger & Surbek (2026). Using Machine Learning to Compute Constrained Optimal Carbon Tax Rules. *Journal of Political Economy: Macroeconomics*, forthcoming |

## References

- Azinovic, M., Gaegauf, L., & Scheidegger, S. (2022). Deep Equilibrium Nets. *International Economic Review*, 63(4), 1471-1525. (available in `lectures/lecture_1/readings/`)
- Chen, H., Didisheim, A., & Scheidegger, S. (2026). Deep Surrogates for Finance: With an Application to Option Pricing. *Journal of Financial Economics*, 177, 104222. (available in `lectures/lecture_2/readings/`)
- Folini, D., Friedl, A., Kuebler, F., & Scheidegger, S. (2024). The Climate in Climate Economics. *Review of Economic Studies*. (available in `lectures/lecture_2/readings/`)
- Friedl, A., Kuebler, F., Scheidegger, S., & Usui, T. (2023). Deep Uncertainty Quantification: With an Application to Integrated Assessment Models. (available in `lectures/lecture_3/readings/`)
- Kuebler, F., Scheidegger, S., & Surbek, O. (2026). Using Machine Learning to Compute Constrained Optimal Carbon Tax Rules. *Journal of Political Economy: Macroeconomics*, forthcoming. (available in `lectures/lecture_3/readings/`)
- Scheidegger, S. & Bilionis, I. (2019). Machine Learning for High-Dimensional Dynamic Stochastic Economies. *Journal of Computational Science*, 33, 68-82. (available in `lectures/lecture_2/readings/`)

## Citation

If you find this course material useful for your research, please cite the
following papers:

```bibtex
@article{azinovic2022deep,
  title={Deep Equilibrium Nets},
  author={Azinovic, Marina and Gaegauf, Luca and Scheidegger, Simon},
  journal={International Economic Review},
  volume={63},
  number={4},
  pages={1471--1525},
  year={2022},
  publisher={Wiley}
}

@article{folini2024climate,
  title={The Climate in Climate Economics},
  author={Folini, Doris and Friedl, Aleksandra and Kuebler, Felix and Scheidegger, Simon},
  journal={Review of Economic Studies},
  year={2024},
  publisher={Oxford University Press}
}

@article{chen2025Deep,
  title={Deep Surrogates for Finance: With an Application to Option Pricing},
  author={Chen, Hui and Didisheim, Antoine and Scheidegger, Simon},
  journal={Journal of Financial Economics},
  volume={177},
  pages={104222},
  year={2026},
  publisher={Elsevier}
}

@article{friedlDeep2023,
  title={Deep Uncertainty Quantification: With an Application to Integrated Assessment Models},
  author={Friedl, Aleksandra and K{\"u}bler, Felix and Scheidegger, Simon and Usui, Takafumi},
  langid={english},
  year={2023}
}

@article{kubler2025using,
  title={Using Machine Learning to Compute Constrained Optimal Carbon Tax Rules},
  author={K{\"u}bler, Felix and Scheidegger, Simon and Surbek, Oliver},
  journal={Journal of Political Economy: Macroeconomics},
  note={forthcoming},
  year={2026}
}

@article{scheidegger2019machine,
  title={Machine Learning for High-Dimensional Dynamic Stochastic Economies},
  author={Scheidegger, Simon and Bilionis, Ilias},
  journal={Journal of Computational Science},
  volume={33},
  pages={68--82},
  year={2019},
  publisher={Elsevier}
}
```

## Lecturer

**Simon Scheidegger**
[HEC, University of Lausanne](https://sischei.github.io)
Visiting Senior Fellow, Grantham Research Institute, London School of Economics

**Practical sessions:** Maria Pia Lombardo

## Errata and feedback

Please report typos, broken links, or substantive issues with the slides,
notebooks, or readings by either:

- opening an issue on the [companion GitHub repository](https://github.com/sischei/cemracs2026_DEQN/issues), or
- emailing [simon.scheidegger@unil.ch](mailto:simon.scheidegger@unil.ch).

Pull requests with fixes are welcome.
