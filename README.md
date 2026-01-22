# Portfolio
#  Customer Support Ticket Optimization – Power BI Dashboard

##  Project Overview
This project analyzes **customer support ticket performance** to evaluate **resolution efficiency, SLA compliance, and customer satisfaction (CSAT)**.  
The dashboard helps stakeholders identify bottlenecks, SLA breaches, and improvement opportunities across agents and ticket priorities.

---

##  Business Problem
Customer support teams often struggle with:
- High **SLA breaches**
- Long **resolution times**
- Low **customer satisfaction**
- Limited visibility into **agent performance**

This project provides a **data-driven solution** to monitor and optimize support operations.

---

##  Key KPIs
- **Total Tickets**
- **Average Resolution Time (hrs)**
- **SLA Compliance %**
- **SLA Breach Count**
- **Average CSAT Score**

---

##  Dashboard Insights
###  Ticket Volume & Priority
- High-priority tickets contribute significantly to total resolution time.
- Critical tickets show the **highest average resolution time**.

###  SLA Performance
- Only **40% SLA compliance**, indicating major process gaps.
- **3 out of 5 tickets breached SLA**, mostly handled by specific agents.

###  Agent Performance
- SLA breaches are concentrated among selected agents.
- Some agents resolve tickets faster while maintaining SLA compliance.

### Customer Satisfaction
- Average CSAT score is **3.0**, signaling room for service quality improvement.

---

## Tools & Technologies
- **Power BI Desktop**
- **DAX** (Measures & Calculations)
- **Excel** (Source Data)
- **Data Modeling & Visualization**

---

## Dataset
- Simulated customer support ticket data  
- Includes:
  - Ticket ID
  - Priority
  - Agent Name
  - Resolution Time
  - SLA Status
  - CSAT Score

---

## Key DAX Measures
```DAX
Avg Resolution Time (hrs) = AVERAGE(Tickets[Resolution_Hours])

SLA Compliance % =
DIVIDE(
    CALCULATE(COUNT(Tickets[Ticket_ID]), Tickets[SLA_Status] = "Met"),
    COUNT(Tickets[Ticket_ID])
)

SLA Breaches =
CALCULATE(COUNT(Tickets[Ticket_ID]), Tickets[SLA_Status] = "Breached")

Total Tickets = COUNT(tickets[Ticket_id])

