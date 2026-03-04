---
title: "Sector-Coupled Capacity Expansion Modeling: Data Centers and Heat Pump Electrification"
collection: portfolio
permalink: /project/data-centers-heat-pumps-affordability
excerpt: "High-resolution capacity expansion framework quantifying interactions between data center load growth, residential electrification, and long-term energy affordability."
---

## Overview

Developed a high-resolution sector-coupled capacity expansion modeling framework to evaluate how rapid data center growth interacts with residential heat pump electrification and energy affordability in the PJM Dominion (PJMD) region.

The framework integrates long-term investment planning, bottom-up sectoral load construction, and retail-territory economic accounting to quantify cross-sector infrastructure and price effects.

---

## Technical Architecture

- National-scale capacity expansion modeling using TEMOA  
- Bottom-up load construction (residential, commercial, industrial, EVs, data centers)  
- 52-week × 168-hour temporal resolution for seasonal fidelity  
- Weather-indexed heating and cooling demand modeling  
- Data center PUE-based load decomposition (≈90% baseload, ≈10% cooling-sensitive)  
- Shadow-price extraction from discounted dual variables  
- Conversion to real $/MWh marginal system costs  
- Retail-territory scaling for bill and NPV accounting  

Model captures:

- Seasonal complementarity between summer-peaking data centers and winter-peaking heat pumps  
- Fuel-switching dynamics between natural gas and electricity  
- Transmission utilization under sectoral load shifts  
- Distributional impacts across customer classes  
- Public-program and private-participant NPV perspectives  

---

## Key Capabilities

- Integrated cross-sector long-term planning within a unified optimization model  
- Explicit modeling of seasonal load complementarity  
- Marginal system cost extraction linked to retail bill impacts  
- Retail-territory NPV framework connecting bulk-system investments to customer outcomes  
- Scenario-based infrastructure adequacy assessment under rapid industrial load growth  

---

## Case Study Configuration

**Region:** Virginia PJM Dominion (PJMD)  
**Data center trajectories:** Low IDC vs High IDC  
**Heat pump pathways:** BAU (50% adoption) vs High Adoption (90%)  
**Horizon:** 2025–2040  

---

## Empirical Impact

- $200–350M reduction in residential energy expenditures by 2040 under high heat pump adoption (≈7–12%)  
- 57% reduction in building-sector natural gas consumption (~15 TWh electrification shift)  
- Only 2–3 GW incremental generation required despite large-scale electrification  
- Improved winter transmission utilization without increasing per-MWh system costs  
- Program NPV up to $2.42B at moderate cost-share levels  
- Demonstrates electrification as economically complementary to industrial load growth  

Results show that coordinated sector coupling can improve infrastructure utilization and reduce consumer costs even under aggressive data center expansion.

---

## Engineering Deliverables

- High-resolution TEMOA capacity expansion model for PJMD  
- Bottom-up sectoral load construction pipeline  
- Data center load parameterization modules  
- Shadow-price extraction and real-price conversion scripts  
- Retail-territory NPV and bill accounting framework  
- Scenario configuration and reproducibility scripts  

---

## Relevance

Positions sector coupling as a planning necessity in regions experiencing simultaneous electrification and hyperscale industrial load growth.

Framework bridges capacity expansion modeling, distributional economics, and infrastructure utilization analysis to inform regulatory and policy decisions under rapid demand transformation.

---

## Related Publication

Khayambashi, K., Kaufman, M., DeCarolis, J., Shobe, W., Wade, C., McCollum, D., Alemazkoor, N., & Clarens, A. F.  
Interactions Between Data Center Load Growth, Residential Heat Pump Adoption, and Energy Affordability.  
*Under review at Joule.*

[Code Repository](https://github.com/kamiarkhayam/Data-Centers-HP-Affordability)
