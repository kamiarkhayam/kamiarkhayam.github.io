---
title: "Sector-Coupled Capacity Expansion Modeling: Data Centers and Heat Pump Electrification"
collection: portfolio
permalink: /project/data-centers-heat-pumps-affordability
excerpt: "High-resolution capacity expansion modeling framework quantifying interactions between data center load growth, building electrification, and energy affordability."
---

This project develops a high-resolution sector-coupled capacity expansion framework to evaluate how rapid data center growth interacts with residential heat pump electrification and energy affordability in the PJM Dominion (PJMD) region.

The system integrates:

• National-scale capacity expansion modeling using TEMOA  
• Bottom-up sectoral load construction (residential, commercial, industrial, EVs, data centers)  
• 52-week × 168-hour temporal structure for seasonal resolution  
• Weather-indexed cooling and heating load modeling  
• Data center PUE-based load decomposition (90% baseload, 10% cooling-sensitive) :contentReference[oaicite:0]{index=0}  
• Shadow-price conversion from discounted dual variables to real $/MWh values  
• Retail-territory scaling for bill and NPV accounting  

The modeling framework explicitly captures:

• Seasonal complementarity between summer-peaking data centers and winter-peaking heat pumps  
• Fuel-switching dynamics between natural gas and electricity  
• Transmission utilization effects under sectoral load shifts  
• Distributional impacts across residential and commercial customers  
• Public-program and private-participant net present value (NPV) perspectives  

Case study configuration:

• Region: Virginia PJM Dominion (PJMD)  
• Data center trajectories: Low IDC, High IDC  
• Heat pump adoption pathways: BAU (50%) vs High Adoption (90%)  
• Horizon: 2025–2040  

Key technical contributions include:

• First capacity-expansion study quantifying system-level interaction between data center growth and building electrification  
• Explicit modeling of seasonal load complementarity within long-term investment planning  
• Bulk-system marginal cost extraction and real-price conversion methodology  
• Retail-territory NPV framework linking system costs to customer bills  

Impact:

• $200–350M reduction in residential energy expenditures by 2040 under high heat pump adoption (~7–12%) :contentReference[oaicite:1]{index=1}  
• 57% reduction in building-sector natural gas consumption (~15 TWh shift to electricity) :contentReference[oaicite:2]{index=2}  
• Only 2–3 GW incremental generation capacity required despite electrification :contentReference[oaicite:3]{index=3}  
• Improved winter transmission utilization without increasing per-MWh system costs  
• Program NPV up to $2.42B at moderate cost-share levels :contentReference[oaicite:4]{index=4}  
• Demonstrates electrification as economically complementary to industrial load growth  

The framework follows a system-coupling paradigm: rather than modeling sectors independently, it quantifies cross-sector load interactions and infrastructure utilization effects within a unified long-term optimization model.

## Related Publication

Khayambashi, K., Kaufman, M., DeCarolis, J., Shobe, W., Wade, C., McCollum, D., Alemazkoor, N., & Clarens, A. F.  
Interactions Between Data Center Load Growth, Residential Heat Pump Adoption, and Energy Affordability.  
*Under review at Joule.*

[Code Repository](https://github.com/kamiarkhayam/Data-Centers-HP-Affordability)
