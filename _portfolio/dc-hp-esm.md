---
title: "Sector-Coupled Capacity Expansion Modeling: Data Centers and Heat Pump Electrification"
collection: portfolio
permalink: /project/data-centers-heat-pumps-affordability
excerpt: "Capacity expansion modeling framework quantifying interactions between hyperscale data center growth, residential electrification, and long-term energy affordability."
---

## Overview

Developed a sector-coupled capacity expansion modeling framework to evaluate how rapid hyperscale data center growth interacts with residential heat pump electrification and energy affordability in the PJM Dominion (PJMD) region.

The model integrates long-term electricity system planning with bottom-up demand modeling to capture cross-sector load interactions and their implications for infrastructure investment and consumer energy costs.

---

## Technical Architecture

The framework combines power system planning with high-resolution demand modeling:

- Capacity expansion modeling using **TEMOA**
- Bottom-up construction of sectoral electricity demand (residential, commercial, industrial, EVs, and data centers)
- High-resolution temporal structure capturing seasonal electricity demand patterns
- Weather-indexed heating and cooling demand modeling
- Data center load decomposition based on power usage effectiveness (PUE)
- Shadow-price extraction from model dual variables to estimate marginal electricity costs
- Retail-territory scaling to translate system-level outcomes into customer bill impacts and net-present-value (NPV) metrics

This architecture allows the model to capture infrastructure investment decisions alongside their downstream economic effects on electricity consumers.

---

## Key Capabilities

- Integrated modeling of electricity demand growth across multiple sectors  
- Representation of seasonal complementarity between emerging loads  
- Evaluation of fuel-switching dynamics between natural gas and electricity  
- Translation of system-level investment outcomes into consumer bill impacts  
- Scenario analysis for infrastructure adequacy under rapid industrial load growth  

---

## Case Study

The framework was applied to the **PJM Dominion region of Virginia**, which is experiencing rapid growth in hyperscale data center electricity demand.

The analysis evaluates interactions between:

- Data center expansion trajectories  
- Residential heat pump adoption pathways  
- Long-term electricity generation and transmission investment  

Scenarios compare baseline adoption with accelerated electrification pathways through 2040.

---

## Empirical Impact

The analysis shows that electrification of residential heating can complement industrial load growth rather than exacerbate system costs.

Key findings include:

- **$200–350 million reduction in residential energy expenditures by 2040** under high heat pump adoption  
- **57% reduction in building-sector natural gas consumption**, corresponding to large-scale electrification of heating demand  
- Only **2–3 GW of additional generation capacity** required despite substantial load growth  
- Improved seasonal utilization of generation and transmission infrastructure  
- Program net present value up to **$2.4 billion** under moderate cost-sharing assumptions  

Results demonstrate that coordinated electrification strategies can improve infrastructure utilization and reduce consumer costs even in regions experiencing rapid data center expansion.

---

## Engineering Deliverables

- High-resolution TEMOA capacity expansion model for the PJM Dominion region  
- Bottom-up electricity demand construction pipeline  
- Data center load parameterization modules  
- System-cost to retail-price conversion workflow  
- Scenario configuration and reproducibility scripts  

---

## Relevance

Rapid data center growth is transforming regional electricity demand patterns. Planning frameworks must therefore account for interactions between emerging industrial loads and electrification of buildings and transportation.

This project demonstrates how sector-coupled modeling can identify synergies between electrification and industrial demand growth, supporting more cost-effective infrastructure planning and energy policy decisions.

---

## Related Publication

Khayambashi, K., Kaufman, M., DeCarolis, J., Shobe, W., Wade, C., McCollum, D., Alemazkoor, N., & Clarens, A. F.  
*Interactions Between Data Center Load Growth, Residential Heat Pump Adoption, and Energy Affordability.*  
Under review at **Joule**.

[Code Repository](https://github.com/kamiarkhayam/Data-Centers-HP-Affordability)
