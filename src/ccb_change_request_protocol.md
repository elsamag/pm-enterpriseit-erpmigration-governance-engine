# Change Control Board (CCB) Protocol & Governance Procedure

> **Enterprise Practice:** Elsamag IT Solutions  
> **Lead Technical Consultant:** Samuel Chinwendu Agu  
> **Target Domain:** Enterprise IT (Legacy ERP System Migration)  
> **Case Study Client:** Apex Global Distribution  
> **System:** Enterprise ERP Migration Governance & Phase-Gate Control System  
> **Standard:** PMI / Enterprise IT Governance Standard  
> **Document Version:** 2.4.0  

---

## 1. Executive Purpose & Scope

The Change Control Board (CCB) protocol establishes a formal, auditable mechanism for managing all changes to the baselined scope, schedule, budget, technical architecture, and system deliverables of the Apex Global Distribution ERP modernization program. This protocol prevents undocumented scope creep, preserves baseline integrity across work breakdown structures (WBS), and guarantees that every project alteration is systematically evaluated against risk, cost, and schedule impacts prior to implementation.

---

## 2. CCB Governance Board Composition & Quorum

### 2.1 Board Membership
The CCB operates as a cross-functional governing authority composed of key project leaders:

| Role | Representative | Voting Mandate | Quorum Weight |
| :--- | :--- | :--- | :--- |
| **Chair / Lead PM & Governance Auditor** | Samuel Chinwendu Agu | Mandatory Voting Member | Presiding / Tie-Break |
| **Enterprise Solution Architect** | Technical Lead | Mandatory Voting Member | Technical Impact |
| **Operations Business Process Owner** | Operations Lead | Mandatory Voting Member | Operational Impact |
| **Information Security & Compliance Lead** | InfoSec Lead | Advisory / Veto on Security | Security Compliance |
| **Executive Sponsor** | Steering Committee Liaison | Escalation Tier 3 Approver | Strategic / Budget Authority |

### 2.2 Meeting Cadence & Quorum Rules
* **Standard Cadence:** Bi-weekly formal review sessions.
* **Quorum Requirement:** 100% attendance/voting participation of mandatory members (or formal designees) is required for binding decisions.
* **Decision Threshold:** Unanimous consensus for Tier 2 impacts; escalated to the Executive Steering Committee for Tier 3 impacts.

---

## 3. Change Classification & Threshold Matrix

Change Requests (CRs) are categorized into three severity tiers based on budget, schedule, and architectural variances:

| Metric | Tier 1 (Minor) | Tier 2 (Moderate) | Tier 3 (Major) |
| :--- | :--- | :--- | :--- |
| **Budget Variance** | < $2,500 USD | $2,500 - $15,000 USD | > $15,000 USD |
| **Schedule Variance** | <= 2 Work Days | 3 - 5 Work Days | > 5 Work Days |
| **Scope Impact** | Task-level nuance | Sprint milestone | Phase-Gate WBS |
| **Approval Authority** | Lead PM / Tech Lead | CCB Board Quorum | Executive Steering Committee |

---

## 4. End-to-End Change Request Lifecycle Workflow

```text
[Initiator]          [Lead Consultant]          [CCB Board]          [PMO / Sprints]
     |                       |                       |                      |
     |-- 1. Submit CR ------>|                       |                      |
     |   (Standard Form)     |-- 2. Triage & Impact->|                      |
     |                       |      Assessment       |                      |
     |                       |                       |-- 3. Convene Review  |
     |                       |                       |      & Vote          |
     |                       |<-- Decision Log ------|                      |
     |                       |   (Approve/Reject)    |                      |
     |<-- 4. Notify ---------|--------------------------------------------->|
     |    Stakeholders       |-- 5. Baseline Re-alignment (WBS, CPM, Cost)->|
```

 ### 4.1 Step-by-Step Procedure

1. **Submission (Step 1):** The requestor completes a standardized Change Request Form documenting the business justification, proposed modification, and affected deliverables.
2. **Impact Assessment (Step 2):** The Lead Technical Consultant and Technical Lead assess the technical feasibility, cost implications, critical path impact, and risk profile.
3. **Formal CCB Review (Step 3):** The board evaluates the CR during the bi-weekly session and renders one of three formal decisions:
   * **APPROVED:** Formal baseline adjustment authorized.
   * **REJECTED:** Closed with recorded rationale in the CCB log.
   * **DEFERRED:** Returned to requestor for additional analysis or deferred to next phase.
4. **Baseline Re-alignment (Step 4):** Upon approval, the Project Manager updates the Integrated Master Schedule (CPM), WBS Dictionary, and cost baselines.
5. **Execution & Audit (Step 5):** The modification is assigned to the appropriate Agile sprint backlog and logged in the project governance audit trail.

---

## 5. Emergency Change Procedure (Fast-Track)

For urgent production-blocking incidents or zero-day security vulnerabilities that cannot await the bi-weekly CCB cycle:

1. **Authorized Emergency Decision Makers:** Dual authorization by **Executive Sponsor + Lead Technical Consultant (Samuel Chinwendu Agu)**.
2. **Execution:** Immediate containment and technical patch deployment.
3. **Retrospective Audit Window:** A formal retrospective CCB audit and documentation sign-off must occur within **48 hours** of emergency deployment.

---

## 6. Standardized Change Request (CR) Form Template

```text
================================================================================
                    ENTERPRISE CHANGE REQUEST (CR) FORM
================================================================================
CR Tracking ID: CR-____                     Date Submitted: YYYY-MM-DD
Requestor Name: __________________________  Department/Role: ___________________
Deliverable Affected: [ ] Data Migration    [ ] ERP Config     [ ] Security/Infra
                      [ ] Interface/API     [ ] UAT Scope      [ ] Other: ______

1. DESCRIPTION OF PROPOSED CHANGE:
   [Detailed technical/functional narrative of the change]

2. BUSINESS JUSTIFICATION & DRIVER:
   [Reason for change, business impact if rejected, regulatory/operational driver]

3. IMPACT ASSESSMENT (Completed by Lead Technical Consultant):
   - Estimated Cost Variance: $_______________ USD
   - Estimated Schedule Variance: +/- _______ Working Days
   - Critical Path Affected: [ ] YES  [ ] NO
   - Security/Compliance Risk Score (1-5): _____

4. CCB DETERMINATION:
   [ ] APPROVED        [ ] REJECTED        [ ] DEFERRED FOR STUDY
   Voting Quorum Record:
   - Lead PM / Governance Auditor: _______________  [Date: _________]
   - Enterprise Solution Architect: ______________  [Date: _________]
   - Operations Process Owner: ___________________  [Date: _________]

5. BASELINE RE-ALIGNMENT SIGN-OFF:
   WBS Updated: [ ] YES   Master Schedule (CPM) Updated: [ ] YES   Budget Adjusted: [ ] YES
================================================================================
```

## 7. Change Control Audit Register Schema

All evaluated change requests are recorded in the central repository audit log:

| CR_ID | Submission_Date | Title_Description | Impact_Tier | Cost_Impact | Schedule_Impact | CCB_Status | Resolution_Date |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| CR-001 | 2026-04-10 | Add Multi-Region Tax Engine API | Tier 2 | +$8,200 | +3 Days | APPROVED | 2026-04-12 |
| CR-002 | 2026-05-02 | Legacy Inventory Custom Field Import | Tier 1 | +$1,100 | 0 Days | APPROVED | 2026-05-03 |
| CR-003 | 2026-05-18 | Out-of-Scope Custom Warehouse Mod | Tier 3 | +$24,000 | +9 Days | REJECTED | 2026-05-20 |

