# Cara Li's Contributions to the 50-State Simulation Project

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

