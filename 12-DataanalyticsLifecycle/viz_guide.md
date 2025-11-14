# Tableau Visualization Summary Guide

This guide summarizes the types of visualizations used in Tableau during the course, with an overview of where they are commonly applied, key techniques or features, and ethical considerations.

---

## 📊 Bar Charts

**Usage:** Comparison across categories (e.g., Sales by Region, Profit by Product)  
**Key Points:** Sorting, color encoding, dual axis, table calculations (e.g., % of total, % difference), groupings, filters  
**Ethical Notes:** Avoid truncating axes, exaggerating differences, or omitting categories.

---

## 📈 Line Charts

**Usage:** Trends over time  
**Key Points:** Continuous dates, dual-axis with bar charts, time grouping parameters, animation settings  
**Ethical Notes:** Clearly indicate cumulative vs per-period values; avoid cherry-picking time frames.

---

## 🔄 Dual Axis Charts

**Usage:** Compare metrics on the same x-axis (e.g., Sales vs Profit over time)  
**Key Points:** Synchronize axes, customize marks, dual-axis formatting  
**Ethical Notes:** Ensure axis scales are synchronized; label both axes clearly to avoid misleading comparisons.

---

## 📍 Maps (Symbol, Filled, Density)

**Usage:** Spatial/geographic analysis (e.g., Sales by State)  
**Key Points:** Custom areas, map layers, background maps, FIXED/EXCLUDE/INCLUDE LoD  
**Ethical Notes:** Avoid misleading color scales or hidden regions; clarify boundaries and units.

---

## 🎯 Scatterplots

**Usage:** Correlation or distribution (e.g., Sales vs Profit)  
**Key Points:** Trend lines, clustering, marginal histograms, animation using Pages  
**Ethical Notes:** Avoid implying causation from correlation; handle outliers transparently.

---

## 📊 Treemaps

**Usage:** Proportional comparison within a hierarchy  
**Key Points:** Nesting by dimensions (e.g., Sub-Category by Segment)  
**Ethical Notes:** Color and size scales should reflect data accurately; avoid confusing hierarchical nesting.

---

## 🎚️ Parameterized Views

**Usage:** Interactive toggling between measures or dimensions  
**Key Points:** Parameters, calculated fields, dynamic time or metric selection  
**Ethical Notes:** Ensure user-selected views are clear; default values should not mislead.

---

## 🧩 Calculated Fields

**Usage:** Derived metrics or custom grouping (e.g., Costs, Profitability, Flags)  
**Key Points:** IF/CASE logic, text functions, LoD, sets  
**Ethical Notes:** Clearly label any calculated fields; avoid hidden manipulations that affect interpretation.

---

## 🔍 Filters

**Usage:** Data exploration or interaction control  
**Key Points:** Context filters, Top N, relative date, apply across worksheets  
**Ethical Notes:** Communicate what is being filtered; avoid misleading partial views.

---

## 📉 Waterfall Charts

**Usage:** Showing incremental values to a total (e.g., Monthly Profit changes)  
**Key Points:** Table calculations, Gantt bars for negative values  
**Ethical Notes:** Label starting and ending points clearly; avoid misrepresenting contributions.

---

## 🗺️ Story / Dashboard

**Usage:** Presentation, interactive analytics  
**Key Points:** Floating vs Tiled, Filter Actions, URL actions, Story Points  
**Ethical Notes:** Keep context visible; avoid cherry-picking visualizations to mislead.

---

## 🚦 KPI Dashboards

**Usage:** Executive summaries  
**Key Points:** LoD for fixed totals, map with KPIs, filters and highlights  
**Ethical Notes:** Avoid emphasizing small differences; provide clear reference points.

---

## 📈 Bump Charts

**Usage:** Rank over time  
**Key Points:** Rank function, line plot with table calculation  
**Ethical Notes:** Clearly label axes; ranks can mislead if underlying values vary greatly.

---

## 🔀 Sets and Combined Sets

**Usage:** Dynamic grouping and filtering (e.g., Top 10, Negative Profit)  
**Key Points:** Parameter control, combining logic, visual comparison  
**Ethical Notes:** Indicate criteria and any exclusions; avoid hiding significant data.

---

## 📆 Cohort Analysis

**Usage:** User segmentation over time  
**Key Points:** Sets based on first purchase, line chart by cohort  
**Ethical Notes:** Clarify cohort definition and data coverage; avoid selective time frames.

---

## 🎨 Custom Icons / Shapes

**Usage:** Visual appeal or clear symbolic distinction  
**Key Points:** Custom shape import, assignment to dimension  
**Ethical Notes:** Avoid misleading symbols or over-emphasis using shapes.

---

## 🎞️ Animated Visuals

**Usage:** Visual transitions for storytelling or change over time  
**Key Points:** Enable animation, duration & style, Pages for interaction  
**Ethical Notes:** Ensure animation does not exaggerate trends; include clear labels.

---

## 🔁 Tableau Extensions (Sankey, Custom Viz)

**Usage:** Advanced custom visualizations  
**Key Points:** Install .trex files, configure data fields, adjust style  
**Ethical Notes:** Verify calculations are transparent; avoid hidden manipulations.

---

## 🔐 Row-Level Security

**Usage:** Data restriction per user  
**Key Points:** USERNAME() function, Access Filter, inner join with user table  
**Ethical Notes:** Ensure permissions are correct; avoid unintentional data exposure.

---

## 🧮 LoD Calculations (FIXED, INCLUDE, EXCLUDE)

**Usage:** Level-specific aggregations  
**Key Points:** Use-case differences (Fixed totals vs excluding dimension)  
**Ethical Notes:** Make clear what is being aggregated; explain table calculations.

---

## 📊 Funnel Charts

**Usage:** Stage-by-stage conversion  
**Key Points:** Sort by process stage, table calculation for % of max  
**Ethical Notes:** Clearly label percentages; avoid hiding stages or exaggerating drop-offs.

---

## 📦 Box Plots

**Usage:** Distribution analysis (e.g., Sales by Region)  
**Key Points:** Disaggregate measures, optional reference lines  
**Ethical Notes:** Label outliers; avoid hiding extreme values that affect interpretation.

---

## ✨ Sparklines

**Usage:** Small, inline trend representation  
**Key Points:** MIN/MAX axes, context lines, table calculations  
**Ethical Notes:** Avoid misleading trends by truncating axes or omitting baseline.

---

## 🔀 Sankey Diagram

**Usage:** Flow between categories (e.g., Customers to Products)  
**Key Points:** Path and measure settings, curved lines, table calculations  
**Ethical Notes:** Avoid overstating flows; scale line thickness proportionally.

---

## 🌞 Dynamic Sunburst

**Usage:** Hierarchical relationships with interactive drilling  
**Key Points:** Set parameters for levels, color by measure  
**Ethical Notes:** Ensure clear labeling of levels; avoid overcomplicating hierarchy.
