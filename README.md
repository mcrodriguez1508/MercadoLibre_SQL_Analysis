# MercadoLibre Funnel & Retention Analysis 🛒📊

## 📝 1. Context & Research Objective
The central objective of this project is to evaluate the efficiency of MercadoLibre's purchasing process, identifying specific friction points where user interest drops.

- **Geographic Scope:** 10 Latin American countries.
- **Period:** January to August 2024.
- **Funnel Definition:** The analysis starts from the initial event **`select_item`** and tracks **cumulative conversions** through to the final transaction. This approach provides clarity on how unique users progress through each logical stage of the flow.

## 🛠 Methodology
- **Tools:** SQL (PostgreSQL) for data extraction and aggregation; Excel for visualization and reporting.
- **Techniques:** Conversion Funnel Analysis and Retention Cohort Analysis.

## 📊 2. Conversion Funnel Analysis
A progressive decline is observed throughout the flow, with a final success rate of **1.25%** starting from 100% of users who select an item.



- **Critical Friction Point:** The most significant user loss occurs during the **`select_item` → `add_to_cart`** transition. Only 15.3% of users who view a product proceed to add it to their cart.
- **Performance by Country:** - **Leader:** **Uruguay** stands out with the highest conversion efficiency (4.55%).
  - **Critical Zones:** Ecuador, Colombia, and Paraguay show a 0% final conversion rate.

## 🔍 3. Regional Variation & Hypotheses
Following the detection of a 0% conversion rate in certain markets, the following **hypotheses for further validation** are proposed (as current data does not support categorical conclusions):
1. **Technical Frictions:** Possible failures in the integration of local payment gateways or loading errors on the purchase button.
2. **Data Volume:** Low traffic in these specific regions might not be statistically representative.
3. **Tracking Inconsistencies:** Potential gaps in the tagging of conversion events for these specific countries.
4. **Trust Barriers:** Users might be in a purely exploratory stage due to unclear shipping costs or seller credibility.

## 🔄 4. Retention Analysis
User loyalty was measured by tracking cohorts at standard milestones: **D7, D14, D21, and D28**.

- **Diagnosis:** There is a healthy initial retention (effective onboarding), but a **severe drop-off is detected after day 21**. 
- **Retention Leaders:** - **Brazil:** Leads in early-stage retention (short-term).
  - **Mexico and Peru:** Show the most solid long-term retention (D28) at approximately 3.1%, suggesting a more loyal user base.

## 💡 5. Business Implications
1. **Lack of Habit Formation:** The product successfully attracts users initially but fails to establish a recurring monthly purchasing habit (the near-total abandonment by day 28 is a critical red flag).
2. **Cart Friction:** Investment focus should not be on increasing top-of-funnel traffic, but rather on improving purchase intent at the `add_to_cart` stage.

## 🧩 6. Personal Reflection & Prioritization
I have prioritized optimizing the **`select_item` → `add_to_cart`** stage for the following reasons:
- This step represents where 85% of potential sales are lost.
- **Proposed Actions:** Improve the visibility of the Call to Action (CTA), provide transparent shipping costs from the first view, and strengthen seller trust badges. Increasing conversion at this point would have a significantly higher ROI than any
