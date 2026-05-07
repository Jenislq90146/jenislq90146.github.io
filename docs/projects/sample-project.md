# Spatio-temporal Interactions Among Carnivores and Prey in the Western Himalaya

![Project overview image](../assets/images/project1-cover.png)

## Overview

Using camera-trap data from 284 stations across ten high-altitude sites in Himachal Pradesh, 
this study examined how trophic and intraguild interactions shape carnivore community structure 
in resource-limited Himalayan landscapes. Contrary to competition-based predictions, carnivore 
species largely co-occurred and tracked prey activity, pointing to a bottom-up control of 
community dynamics driven by prey availability rather than apex-predator suppression.

**Study Area:** Himachal Pradesh, India (Northwestern Himalayan shrubland and meadows, >2000 m elevation, ~26,000 km²)  
**Duration:** 2016 – 2019  
**Role:** Lead author — conceived study, analysed data, led writing  
**Status:** Published — *Journal of Zoology* 322 (2024): 3–11. DOI: [10.1111/jzo.13120](https://doi.org/10.1111/jzo.13120)

---

## Methods & Tools

**Data Sources**

- Camera-trap detections of 6 carnivore species and prey across 10 sites (284 stations, 60-day deployments per site)
- Enhanced Vegetation Index (EVI) from remote sensing, averaged within 500 m of each camera station
- Multiscale Topographic Position Index (mTPI) as a detection covariate

**Processing Steps**

1. Curated and tagged camera-trap images in Digikam; generated species detection histories using `camtrapR` in R
2. Converted detections to detection–nondetection matrices at the daily sampling occasion level
3. Fitted multi-species occupancy models (Rota et al. 2016) to assess co-occurrence and conditional occupancy along a productivity gradient
4. Estimated pairwise spatial interactions (Species Interaction Factor, SIF) using Bayesian two-species occupancy models (`wiqid`, `jagsUI`) with 3 MCMC chains of 10,000 iterations
5. Estimated temporal overlap of activity patterns for 24 carnivore and prey pairs using kernel density functions (`overlap` package; Δ̂₁ index)

**Tools Used**

| Tool | Purpose |
|------|---------|
| R (`camtrapR`) | Camera-trap data management and detection history generation |
| R (`wiqid`, `jagsUI`) | Bayesian multi-species occupancy modelling |
| R (`overlap`) | Kernel density estimation of diel activity overlap |
| Digikam | Image tagging and species identification |
| Google Earth Engine | EVI extraction for productivity covariate |

---

## Key Findings

- 11 of 15 carnivore pairs showed **positive spatial associations** (mean SIF = 1.47; 95% CI: 1.16–1.78), contrary to competition-based predictions of segregation in resource-poor environments
- 8 of 9 carnivore–prey pairs showed **positive spatial associations** (mean SIF = 1.99), stronger than intraguild carnivore associations — indicating prey availability as the primary community-structuring force
- **Temporal avoidance** was observed in only 4 of 15 carnivore pairs (e.g., red fox–mountain weasel, stone marten–mountain weasel), suggesting temporal rather than spatial partitioning as the secondary coexistence mechanism
- Red fox and snow leopard showed a strong positive spatio-temporal association, consistent with **carrion provisioning** by apex predators subsidising mesopredators in low-productivity landscapes
- The top-ranked occupancy model was the intercept-only model (no covariates), indicating that **species interactions**, rather than productivity gradients, are the dominant driver of community structure at this site
- Results support a **bottom-up view** of Himalayan carnivore community dynamics — carnivores track prey, not other predators

---

## Links

[Read the Paper (DOI)](https://doi.org/10.1111/jzo.13120){ .md-button }
[View Code on GitHub](https://github.com/Jenislq90146/[YOUR-REPO-NAME]){ .md-button }
