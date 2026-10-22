# Two Spheres of Korean Politics: Knowledge Production and Dissemination across Linguistic Divides

**Authors:** Hyowon Kim, Do Won Kim, and Won-ho Park  
**Status:** Manuscript under review at *Humanities & Social Sciences Communications*.

## Overview

This study examines how knowledge production and dissemination differ across Korean and English linguistic spheres, using research on Korean politics as a case. It analyzes article metadata, research topics, outgoing references, and incoming citations. Linguistic spheres are operationalized by written language, journal indexing, and publisher location.

## Research question and hypotheses

- **RQ1 — Knowledge production:** How are research topics on Korean politics distributed across linguistic spheres? BERTopic uses English abstracts to identify topics. Topic skew is measured using the Normalized Difference Score (NDS); positive values indicate greater prevalence in the Korean sphere and negative values indicate greater prevalence in the English sphere.
- **H2-a — Local references:** Korean-sphere articles are expected to cite a higher proportion of references from the same sphere.
- **H2-b — Shared references:** English-sphere articles are expected to cite references more frequently cited across both linguistic spheres.
- **H3-a — Visibility:** English-sphere articles are expected to receive more citations.
- **H3-b — Locality:** Korean-sphere articles are expected to receive a higher proportion of citations from within the Korean sphere.
- **H3-c — Prestige:** English-sphere articles are expected to receive citations from outlets with higher citation-based prestige metrics.

H2 and H3 compare the spheres using Mann–Whitney U tests. The main manuscript presents results by written language; the supplementary material also reports comparisons by journal indexing and publisher location.

## Data and analysis

The source corpus contains **15,268 articles**: **10,477 written in Korean** and **4,791 written in English**, across **247 journals**. Written language refers to the article language; English abstracts are used for topic modeling in both groups.

- **RQ1:** The archived 35-label topic classification includes an outlier category and 34 substantive topics. Topic-level NDS uses 9,247 articles assigned to substantive topics, excluding outliers and articles without a topic assignment.
- **H2:** The outgoing citation network contains 385,164 reference links from 12,909 source articles to 232,733 unique referenced works.
- **H3:** The incoming citation network contains 89,926 citation links to 10,621 source articles from 48,655 unique citing works.

Outgoing and incoming citation networks are constructed and analyzed separately. Source-article identifiers connect each network to article metadata. Sample sizes for individual measures vary with metadata availability.

The data-and-code package separates descriptive statistics, RQ1, H2, and H3 into independent Python scripts and includes variable definitions and an analysis guide. A persistent Harvard Dataverse link will be added once available.

## Supplementary material

[View or download the supplementary material (PDF)](supplementary_material.pdf)

- **A. Journal Lists**
- **B. Author-Level Descriptives**
- **C. Topic Distribution:** topic frequencies and proportions, topic keywords, and temporal NDS figures for journal indexing and publisher location
- **D. Hypothesis Testing Results:** Mann–Whitney U results for written language, journal indexing, and publisher location

## Interactive topic map

The original notebook generates an interactive BERTopic map using `topic_model_35.visualize_topics()` and exports it as `topic_map_35topics.html`. The map presents the relative positions and sizes of topics. A browser-viewable link will be added after the archived map HTML is uploaded and hosting is enabled.

The map uses internal model topic identifiers, which may differ from remapped identifiers in exported topic tables. It is separate from the topic-level NDS analysis.

## Reproducibility

The RQ1 analysis uses supplied archived topic assignments. Optional model-fitting code uses English abstracts, but a fresh fit may produce different assignments and map positions because of stochastic components and differences in software versions and computational environments.

## Contact

Hyowon Kim, University of Arizona  
eclair7b@gmail.com
