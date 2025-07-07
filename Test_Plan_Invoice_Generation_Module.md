# 🧪 Test Plan: Invoice Generation Module

**Project Name:** Corcentric Invoice-to-Cash Automation  
**Module Name:** Invoice Generation  
**Created By:** Leena Barua, QA Lead  
**Document Version:** 1.0  
**Date:** July 7, 2025

---

## 1. Objective

To validate that the Invoice Generation module accurately generates invoices based on input data, applying correct formatting, business rules, taxes, and discounts before sending them to clients or systems.

---

## 2. Scope

### ✅ In-Scope:
- Manual creation of invoices via UI
- Auto-generation of invoices from scheduled jobs
- Field validation (e.g., amounts, customer info)
- PDF generation
- Email dispatch confirmation
- Integration with billing and tax systems

### ❌ Out-of-Scope:
- Payment processing (covered in Payment module)
- External tax engine testing

---

## 3. Test Items

- Invoice creation form (UI)
- Scheduled batch invoice job
- PDF invoice rendering
- Invoice status updates
- Logs & audit trail
- API for invoice creation (if available)

---

## 4. Entry Criteria

- Dev has delivered the invoice generation feature to QA
- Test environment is configured and stable
- Test data is prepared
- All blockers from previous sprint resolved

---

## 5. Exit Criteria

- All planned test cases executed
- No high/critical bugs open
- Regression passed
- UAT feedback incorporated

---

## 6. Test Design Techniques

- Equivalence Partitioning (valid/invalid input fields)
- Boundary Value Analysis (amount limits, date ranges)
- State Transition (draft → approved → sent)
- Error Guessing (missing tax ID, null amounts)

---

## 7. Types of Testing

- Functional Testing  
- Field Validation Testing  
- PDF Rendering Validation  
- Integration Testing (billing/tax systems)  
- Negative Testing  
- UI Testing  
- Smoke & Regression Testing

---

## 8. Test Environment

- QA URL: `https://qa.corcentric-invoice.com`  
- Database: QA_SQL_CORCENTRIC  
- Email Server: MockSMTP for email dispatch verification  
- Browser: Chrome latest

---

## 9. Test Deliverables

- Test Scenarios and Test Cases (Excel or Zephyr)  
- Daily Test Execution Report  
- Defect Reports (JIRA)  
- Final Test Summary Report  
- Sign-off Document

---

## 10. Effort Estimation

| Task                        | Effort (Person-Days) |
|-----------------------------|----------------------|
| Test Case Design            | 2                    |
| Test Execution              | 3                    |
| Bug Reporting & Re-testing  | 2                    |
| Review & Reporting          | 1                    |
| **Total**                   | **8 Days**           |

---

## 11. Risks & Mitigation

| Risk | Mitigation |
|------|------------|
| API for tax not ready | Mock API or delay testing |
| PDF layout changes last minute | Validate layout using early drafts |
| Email server not configured | Use local mail capture tool |

---

## 12. Roles & Responsibilities

- **QA Lead (You):** Prepare plan, assign testers, report status
- **Manual QA:** Execute tests, log defects
- **Dev:** Fix bugs, provide clarifications
- **Project Manager:** Coordinate release timelines

---

## 13. Priority Features to Test

| Feature | Priority |
|---------|----------|
| Manual Invoice Creation | Must Have |
| Auto-Generation Job | Must Have |
| Tax/Discount Calculation | Must Have |
| PDF Rendering | Should Have |
| Email Sending | Should Have |
| API Endpoint (if ready) | Could Have |

---

## 14. Approval

| Name         | Role       | Signature |
|--------------|------------|-----------|
| Leena Barua  | QA Lead    | ✅         |
| PM Name      | Project Manager | ✅     |
| Dev Lead     | Development | ✅        |

