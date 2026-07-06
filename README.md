# The Branch Closure Crisis: Mapping the Decline of Physical Banking Access Across UK Communities

## Overview
This project analyses the decline of physical bank branches across the UK between 2015 and 2025, using an open dataset covering every tracked bank and building society branch in the country. The analysis looks at how closures have changed over time, and identifies which towns and regions have lost the largest share of their banking infrastructure.

The objective was to clean and explore a large, real-world dataset, resolve data quality issues as they appeared, and build a clear picture of where physical banking access has declined the most across the UK, covering data cleaning, exploratory analysis, and visualisations at both town and regional level.

&nbsp;

## Why This Project Matters
Branch closures have become one of the most widely discussed issues in UK retail banking, with consumer groups, regulators and MPs raising concerns about communities being left without local access to cash and in person banking services. Despite this attention, it is not always clear which parts of the country have actually been affected the most.

This project was built to demonstrate the ability to take a real, publicly discussed issue and turn it into a structured analytical project, using Python to clean a messy real-world dataset, work through data quality problems as they appeared, and produce findings that could genuinely inform a conversation about banking access in the UK.

&nbsp;

## Dataset
Data was sourced from Geolytix's UK Open Bank Branches dataset (CC0 Licence), a single CSV file containing 12,045 records across 18 columns. The dataset covers every tracked bank and building society branch across the UK, including branches that are open, permanently closed, or in the process of closing, since 2015. Fields include brand, branch type, full address, town, region, postcode, coordinates, current status, and the month and year a branch opened or closed.

The dataset presented several data quality issues that needed to be resolved before analysis, including missing values across region, branch name and address fields, and a small number of clearly incorrect closure years, including values such as 6, 7 and 20220116, which needed to be identified and removed. These issues reflected the kind of real world data quality problems typically encountered before any analysis can begin.

&nbsp;

## Methodology

**1) Load and Inspect the Data:** The dataset was loaded and given an initial first look to confirm its structure, size, and the type of values and gaps present, alongside a check that every column had been assigned the correct data type.

**2) Clean the Data:** Records missing a status, branch type or region were removed, since these are the three fields the whole analysis relies on. Closing branches were combined with Closed branches, and three clearly incorrect closure year values were identified and removed after they caused an unreadable chart.

**3) Explore Closures Over Time:** Branch closures were plotted by year to understand the pace of closures nationally. This revealed a rising trend from 2015 onward, a dip during 2020, and a peak in 2022.

**4) Analyse Closures at Town Level:** Branches were grouped by town to measure how many had closed in each. Towns were ranked by number of closed branches, since ranking by rate alone was found to be unreliable for towns with very few branches.

**5) Analyse Closures at Regional Level:** The same grouping and ranking approach was applied across all 12 UK regions, to test whether the pattern seen at town level held at a wider geographic level.

**6) Summarise Key Insights:** Findings from the time trend, town level and regional analysis were combined into a short summary of where and how physical banking access has declined the most across the UK.

&nbsp;

## Outcomes








## Limitations
**1) Data Time Range:** The dataset only covers 2015 to 2025, so it is not possible to tell whether the rise in closures seen from 2017 onward was already under way before the dataset begins. The 2025 figures may also be incomplete depending on when the dataset was last updated, which affects any comparison with 2024.

**2) Closure Rate at Small Sample Sizes:** Closure rate becomes unreliable for towns with very few branches, since a small number of closures can push the rate to 100%. For this reason, towns are ranked by the number of closed branches rather than closure rate in this project.

**3) No Population Context:** Closure rate measures the share of a town or region's own branches that have closed. It does not account for population, so it does not fully capture how many people are actually affected by reduced access.

**4) No Explanation for Closures:** The dataset records what has closed, not why, so differences between regions or towns should not be read as having a single underlying cause.

**5) Closing Branches Treated as Closed:** Branches marked as Closing were combined with Closed branches, since they are already confirmed for closure. Their exact closure date may not yet be finalised in the source data.
