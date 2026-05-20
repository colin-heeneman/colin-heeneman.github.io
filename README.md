# Colin Heeneman — Research Portfolio

**Live site:** [colin-heeneman.github.io](https://colin-heeneman.github.io)

A Quarto-based research portfolio presenting quantitative policy analysis projects, built for an audience interested in reviewing my early-career public policy research. Deployed via GitHub Pages from the `gh-pages` branch using `quarto publish gh-pages`.

---

## Projects

### ADA-PARC Project
Descriptive analysis of quality-of-life disparities between people with and without disabilities across U.S. geographies. Uses American Community Survey (ACS 5-year) data across four thematic domains: Demographics, Community Living, Community Participation, and Work and Economics. Paired with an interactive Shiny application and Tableau dashboard.

**Source:** `projects/ada-parc.qmd`

### Medicaid Expansion Project
Staggered difference-in-differences analysis using the Callaway-Sant'Anna (2021) estimator to identify the causal effect of ACA Medicaid expansion on uninsured rates and cost-related care avoidance among non-elderly adults. Uses individual-level ACS and state-level BRFSS data.

**Source:** `projects/medicaid-expansion.qmd`

### WIC Program Evaluation Project
Regression discontinuity design (RDD) exploiting WIC's income-eligibility threshold to estimate the program's effect on infant birth weight. Demonstrates applied quasi-experimental methods using synthetic data as a proof-of-concept for program evaluation design.

**Source:** `projects/wic.qmd`

---

## Stack

| Tool | Role |
|---|---|
| [Quarto](https://quarto.org) | Site framework and rendering |
| R | Analysis and report generation |
| [renv](https://rstudio.github.io/renv/) | Reproducible R package environment |
| GitHub Pages | Hosting (`gh-pages` branch) |

---

## Repository Structure

```
.
+-- _quarto.yml              # Site configuration
+-- index.qmd                # Home page
+-- about.qmd                # About page
+-- projects.qmd             # Projects index
+-- research-statement.qmd   # Research statement
+-- cv.qmd                   # CV page
+-- styles.css               # Custom CSS (EB Garamond, palette)
+-- EB_Garamond/             # Bundled font files
+-- files/                   # Static file assets (CV PDF)
+-- projects/
|   +-- ada-parc.qmd                    # ADA-PARC project page
|   +-- ada-parc-descriptive-2023.html  # Full interactive report (iframed)
|   +-- ada-parc-report.pdf             # PDF version
|   +-- medicaid-expansion.qmd          # Medicaid project page
|   +-- medicaid-expansion-did.html     # DiD analysis report (iframed)
|   +-- medicaid-policy-brief.html      # Policy brief (iframed)
|   +-- medicaid-expansion-report.html  # Supplemental report
|   +-- wic.qmd                         # WIC project page
|   +-- wic-no-code.html                # WIC report no-code version (iframed)
|   +-- wic-report.pdf                  # PDF version
+-- renv/                    # renv environment
+-- renv.lock                # Package lockfile
```

---

## Rendering Locally

Requires R and Quarto installed. To restore the R package environment and render the site:

```r
# In R, from the project root
renv::restore()
```

```bash
# From the terminal
quarto render
```

The rendered site outputs to `_site/`. To preview with a local server:

```bash
quarto preview
```

---

## Deployment

The site is deployed to the `gh-pages` branch via:

```bash
quarto publish gh-pages
```

Source files live on `main`. The `_site/` build directory is gitignored on `main` and managed entirely by `quarto publish`.
