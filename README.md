# 📊 Live Interactive Dashboard: https://raishaldhawan23.github.io/Real-Time-Warehouse-Pallet-Flow-Power-BI-Dashboard---DHL-SUPPLY-CHAIN/
## *Click the link above to open the fully interactive Power BI report, where you can click filters, slicers, and explore the live metrics.*


# Real Time Warehouse Pallet Flow (Power BI) Dashboard - DHL SUPPLY CHAIN

## 1. Executive Summary

This project presents a real-time operational dashboard developed as part of a technical task for DHL Supply Chain.

The objective was to provide warehouse managers with immediate visibility into pallet movements entering and leaving the warehouse, enabling faster operational decisions during shift meetings.

The dashboard tracks:

- Inbound pallet movements
- Outbound pallet movements
- Net warehouse movement
- Shift performance
- Regional activity
- Daily movement trends

Interactive filters allow managers to analyse pallet activity across different periods, shifts and regions, helping identify bottlenecks, workload imbalances and warehouse stock accumulation patterns.

---

## 2. Project Background

### Business Context

Warehouse operations depend heavily on the efficient movement of pallets entering and leaving the facility.

However, managers often struggle to answer operational questions quickly:

- Is the warehouse receiving more pallets than it dispatches?
- Which shift handles the highest workload?
- Which hours experience operational peaks?
- Are certain regions contributing disproportionately to warehouse traffic?
- Is warehouse inventory accumulating or reducing over time?

Without a unified dashboard, these questions require manual reporting, delaying decisions and reducing operational visibility.

This project addresses these challenges by building a real-time Power BI dashboard that consolidates inbound and outbound pallet scans into a single operational view.

### Business Objectives

The dashboard was designed to:

- Monitor total pallets entering the warehouse.
- Monitor total pallets leaving the warehouse.
- Track pallet movements hourly.
- Compare operational workloads across shifts.
- Analyse pallet movements by region.
- Identify warehouse inflow and outflow imbalances.
- Support real-time operational decision-making.

---   

## 3. Methodology

### Business Understanding

Defined the goal as providing real-time visibility into pallet movements (IN vs OUT) to support site managers in daily shift meetings. The focus was on tracking pallet volumes by hour, shift, and region, with filters for flexible analysis. 

### Data Understanding

Two datasets were provided:

- Inbound pallet scans
- Outbound pallet scans

The datasets contained: Scan timestamps, Pallet counts, Regions, Delivery locations, Tour information

### Data Preparation
A three-step data quality framework was applied:

#### Profiling:
- Reviewed null values
- Checked duplicates
- Validated timestamp fields
- Assessed pallet count distributions

#### Cleaning:
- Standardised inbound and outbound timestamps
- Created Direction field (IN / OUT)
- Converted pallet counts to integers
- Derived: Hour, Shift, Week, Month, Year, and Integration

Both datasets were appended into a unified fact table to simplify reporting and improve performance.

### Dashboard Design:

<img width="1452" height="812" alt="image" src="https://github.com/user-attachments/assets/a780aa43-82a6-4616-9e58-cd9d9af471b9" />


The dashboard was intentionally designed as a single operational page so managers can obtain insights within seconds.

It contains:

- KPI Cards
- Total Pallets
- Total Pallets OUT
- Total Pallets IN
- Net Movement

### Operational Charts:

#### A. Pallet Movements By Hour
Allows managers to identify:

- Peak inbound periods
- Peak outbound periods
- Potential congestion hours

#### B. Pallets By Shift
Compares:

- Morning Shift
- Afternoon Shift
- Late Shift
to understand operational workload distribution.

#### C. Trend Over Time
Tracks:

- Daily pallet movement trends
- Operational surges
- Volume fluctuations

#### D. Pallets By Region
Highlights:

- Geographic contribution to warehouse activity
- Regional concentration patterns

---

## 4. Key Findings & Business Insights

### 1. Warehouse Inventory is Accumulating Faster than It is Being Dispatched

The dashboard revealed:

| KPI               |  Value |
| ----------------- | -----: |
| Total Pallets IN  |  7,414 |
| Total Pallets OUT |  5,687 |
| Net Movement      | +1,727 |

This positive net movement indicates that more pallets are entering the warehouse than leaving it. While this may initially appear positive from a stock availability perspective, it creates an operational concern: warehouse inventory is gradually accumulating.

If this imbalance continues over multiple days, managers may face:

- Storage capacity constraints
- Congestion in loading and unloading areas
- Reduced operational efficiency
- Increased handling and storage costs

**Business implication:**
The dashboard provides an early warning signal, enabling managers to investigate whether outbound capacity, staffing levels, or transportation schedules need adjustment before warehouse space becomes constrained.

---

### 2. Inbound and Outbound Peaks are Operationally Misaligned

<img width="1776" height="847" alt="image" src="https://github.com/user-attachments/assets/39b282d2-0177-4189-b12c-3ea56db8d595" />


The hourly movement analysis uncovered a significant operational pattern.

The inbound flow experiences major spikes during late evening hours, while outbound pallet movements peak much later, often during the following morning shift.

This means:

* Pallets enter the warehouse faster than they leave during certain periods.
* Inventory temporarily accumulates overnight.
* Storage areas experience additional pressure.
* Material handling equipment may remain underutilised during some periods and overutilised during others.

The pattern is not merely a volume issue.

It is a **timing issue**.

Even when total inbound and outbound volumes appear manageable, poor synchronisation creates operational bottlenecks.

**Business implication:**
Managers can use this insight to rebalance labour schedules, forklift allocation, and transportation timings to smooth pallet flow across the day and minimise overnight congestion.

---

### 3. Late Shift Carries the Highest Operational Workload

The shift analysis shows a clear concentration of workload:

| Shift     | Pallets Processed |
| --------- | ----------------: |
| Late      |              5.3K |
| Morning   |              4.2K |
| Afternoon |              3.6K |

The Late Shift processes the highest pallet volume, making it the most operationally intensive period of the day.

Interestingly, Morning shifts show a stronger outbound orientation, indicating that warehouse teams spend mornings dispatching pallets that accumulated overnight.

This creates a cyclical dependency:

Late Shift → Warehouse receives pallets
Morning Shift → Warehouse clears accumulated inventory

**Business implication:**

This insight helps managers:

* Allocate more warehouse staff during late shifts.
* Increase forklift availability during peak inbound periods.
* Schedule outbound resources more effectively during mornings.
* Prevent labour shortages during the warehouse's busiest periods.

Rather than distributing labour evenly across shifts, staffing can be aligned with actual operational demand.

---

### 4. UK Operations Drive the Majority of Warehouse Activity

<img width="1772" height="772" alt="image" src="https://github.com/user-attachments/assets/9bd5bf0e-3aa2-4fc7-91f8-0cfcc0b75d6b" />


Regional analysis revealed a significant concentration of pallet movement:

| Region | Pallets |
| ------ | ------: |
| UK     |   11.2K |
| Europe |    1.9K |

More than 80% of pallet activity originates from UK operations.

This means that operational inefficiencies occurring in the UK will have a substantially larger impact on overall warehouse performance than issues arising from European operations.

The dashboard therefore, helps prioritise management attention.

**Business implication:**

If:

* Congestion increases,
* Service levels deteriorate,
* Inbound surges become difficult to manage,

The first area requiring operational intervention is the UK warehouse activity.

Managers can focus on staffing, transportation coordination, and process improvements where they create the greatest business impact.

---

### 5. Daily Trends Reveal Persistent Warehouse Build-Up

<img width="1766" height="762" alt="image" src="https://github.com/user-attachments/assets/b04ccbf5-7c5f-4b2f-a495-e7ca6144c04f" />


The trend-over-time chart highlights another important operational pattern.

Over multiple days, inbound pallet volumes consistently exceed outbound volumes.

This indicates that the inventory accumulation observed in the KPI cards is not an isolated event but an ongoing operational trend.

Without visibility, this issue could remain unnoticed until:

* Warehouse space becomes constrained.
* Picking efficiency decreases.
* Labour productivity declines.
* Storage costs increase.

The dashboard transforms this from a reactive problem into a proactive management opportunity.

**Business implication:**

Managers can continuously monitor:

* Daily net pallet movement
* Growth in warehouse inventory
* Emerging bottlenecks
* Capacity risks

and intervene early before operational performance is affected.

---

### Overall Business Story

The dashboard shows that DHL is not facing a shortage of operational activity.

The challenge lies in balancing inbound and outbound pallet movements efficiently.

The analysis reveals three interconnected issues:

* Inbound pallets consistently exceed outbound volumes.
* Late shifts absorb the majority of incoming traffic.
* UK operations dominate overall warehouse activity.

Together, these patterns create inventory build-up and increase the risk of congestion.

By making these relationships visible in real time, the dashboard enables site managers to shift from reactive firefighting to proactive operational planning, improving warehouse flow, resource allocation, and decision-making speed.

--- 

## 5. Data Challenges & Assumptions
### Assumptions

1. Decimal pallet counts were converted to whole pallets.
2. Zero pallet records were retained as valid business events.
3. Carton and non-pallet media types were excluded from dashboard visuals.
4. Missing Tour IDs were excluded because they did not affect operational KPIs.

### Data Challenges

1. Different timestamp formats across inbound and outbound datasets.
2. Null pallet counts in outbound scans.
3. Missing delivery information in several records.
4. Data standardisation was required before combining both datasets.

## 6. Tools and Analytical Capabilities
### Tools

- Power BI
- Power Query
- DAX
- Power Query 

### Data Modelling & Analytics

- Star Schema Modelling
- Data Modelling
- Time Intelligence
- Data Cleaning & Validation
- Data Visualisation
- KPI Design

### Frameworks & Methodologies

- CRISP-DM
