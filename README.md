# 50-State Simulation Project

## Cara Li's contributions

I contributed state-legislative redistricting analyses to the [ALARM Project's 50-State Simulation Project](https://github.com/alarm-redist/fifty-states), an open-source effort to make reproducible redistricting simulations available to researchers and the public.

My work covers the full analysis pipeline in R:

`raw election + Census data` → `geospatial preparation` → `legal and algorithmic constraints` → `SMC simulation` → `convergence and quality validation`

### Merged analysis: South Carolina

My [South Carolina State House/Senate analysis](https://github.com/alarm-redist/fifty-states/pull/267) was merged into the upstream repository in December 2025. The five-file workflow:

- joins Census voting-tabulation-district geometry, election data, municipalities, prior districts, and the enacted plan;
- transforms and simplifies spatial data and constructs the district adjacency graph;
- encodes a 5% population-deviation threshold and county/municipality preservation constraints;
- runs five independent sequential Monte Carlo simulations per chamber with merge-split MCMC steps;
- generates 27,500 plans and retains 20,000 after thinning; and
- evaluates convergence, effective sample size, acceptance rates, and plan diversity.

### Additional upstream submissions

| State | Pull request | Status as of July 2026 |
|---|---|---|
| Alabama | [#250](https://github.com/alarm-redist/fifty-states/pull/250) | Open |
| Alabama BVAP analysis | [#262](https://github.com/alarm-redist/fifty-states/pull/262) | Closed |
| Virginia | [#258](https://github.com/alarm-redist/fifty-states/pull/258) | Open |
| Kentucky | [#245](https://github.com/alarm-redist/fifty-states/pull/245) | Open |
| Indiana | [#244](https://github.com/alarm-redist/fifty-states/pull/244) | Open |
| Indiana baseline | [#238](https://github.com/alarm-redist/fifty-states/pull/238) | Closed |
| Iowa | [#237](https://github.com/alarm-redist/fifty-states/pull/237) | Closed |

Technologies: **R, dplyr, sf, redist, geomander, reproducible simulation pipelines, geospatial data, SMC/MCMC validation**.

---

### The ALARM Project

[![License: CC0 1.0](https://img.shields.io/badge/Data%20License-Public%20domain-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![License: MIT](https://img.shields.io/badge/Software%20License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Dataverse DOI](https://img.shields.io/badge/Dataverse-10.7910%2FDVN%2FSLCD3E-orange)](https://doi.org/10.7910/DVN/SLCD3E)
[![arXiv](https://img.shields.io/badge/arXiv-2206.10763-66a61e.svg)](https://arxiv.org/abs/2206.10763)

Every decade following the Census, states and municipalities must redraw districts for Congress, state houses, city councils, and more. The 50-State Simulation Project enables researchers, practitioners, and the general public to use redistricting simulation analysis to evaluate enacted districts.

The upstream repository contains code to sample districting plans for all 50 U.S. states according to relevant legal requirements. See the [upstream README](https://github.com/alarm-redist/fifty-states#readme), [contribution guidelines](https://github.com/alarm-redist/fifty-states/blob/main/CONTRIBUTING.md), and [Harvard Dataverse](https://doi.org/10.7910/DVN/SLCD3E) for the complete project documentation and data.
