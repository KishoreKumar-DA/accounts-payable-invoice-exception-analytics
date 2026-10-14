# Accounts Payable & Invoice Exception Analytics

## Project Overview

This project analyzes Accounts Payable (AP) invoice and payment records using Microsoft Excel. It focuses on invoice reconciliation, duplicate invoice submissions, payment status monitoring, payment exceptions, and overdue vendor balances.

The objective is to demonstrate how Excel can support finance operations through structured data analysis, exception reporting, and dashboard-based monitoring.

**Note:** This is a portfolio simulation using synthetic data. It is not based on Amazon's internal systems, Oracle records, or actual vendor transactions.

## Business Objectives

- Identify potential duplicate invoice submissions.
- Reconcile invoice amounts against successful payments.
- Categorize invoices by payment status and exception type.
- Monitor overdue invoices and outstanding balances by vendor.
- Build a dashboard to support operational reporting and follow-up prioritization.

## Tools & Technologies

- Microsoft Excel
- Excel formulas: `IF`, `COUNTIF`, `COUNTIFS`, `SUMIFS`, `AND`
- Excel Tables and structured data organization
- PivotTables and PivotCharts
- KPI reporting and dashboard visualization
- Conditional formatting and data validation techniques

## Workbook Structure

| Worksheet | Purpose |
|---|---|
| Invoices_Raw | Source invoice records |
| Payments_Raw | Payment attempts, statuses, and amounts |
| Vendor_Master | Vendor reference information |
| Modification_Requests | Invoice modification request records |
| Data_Dictionary | Field definitions |
| Invoice_Analysis | Invoice reconciliation and exception calculations |
| PT_Exceptions | Summary of assigned invoice exception categories |
| PT_Payments | Summary of invoice payment statuses |
| PT_Overdue | Overdue balances grouped by vendor |
| AP_Dashboard | KPI cards and charts for AP monitoring |

## Key Analysis & Business Rules

### 1. Duplicate Invoice Detection

Identifies repeated combinations of vendor ID and invoice number. These records are flagged for review as potential duplicate submissions rather than automatically confirmed duplicate liabilities.

### 2. Payment Reconciliation

Calculates successful payments associated with each invoice and compares the total paid amount with the invoice amount.

**Amount Difference = Invoice Amount − Total Successful Payments**

A positive difference indicates an outstanding amount, zero indicates the invoice amount has been covered, and a negative difference indicates a potential overpayment.

### 3. Payment Status Monitoring

Categorizes invoice records into payment statuses such as Paid, Partial Payment, Failed, Pending, and Unpaid.

### 4. Exception Classification

Assigns an exception category to each invoice record, including Duplicate Invoice, Failed Payment, Pending Payment, Unpaid Invoice, Amount Mismatch, or No Exception.

The current classification prioritizes duplicate invoices before payment-related exceptions. Consequently, an invoice with multiple issues receives one primary category in the exception chart.

### 5. Overdue Invoice Monitoring

Flags invoices whose due dates have passed as of **14 October 2026** and whose calculated payment status is not Paid.

Overdue balances are summarized by vendor to support prioritization of follow-up activities.

## Dashboard KPIs

The completed dashboard reports the following results from the synthetic dataset:

| KPI | Result |
|---|---:|
| Total Invoice Records | 524 |
| Exception Invoice Records | 48 |
| Overdue Invoice Records | 198 |
| Exception Rate | 9.2% |

**Exception Rate = Exception Invoice Records ÷ Total Invoice Records**

The dashboard also includes:

- Invoice Payment Status
- Invoice Exception Breakdown
- Overdue Balance by Vendor

### Payment Status Results

| Payment Status | Invoice Records |
|---|---:|
| Paid | 322 |
| Unpaid | 104 |
| Pending | 45 |
| Failed | 40 |
| Partial Payment | 13 |

These categories describe the assigned payment status of invoice records. They should not be interpreted as independent payment-attempt counts.

## Business Value

This project demonstrates how spreadsheet-based analysis can help finance operations teams:

- Improve visibility into invoice and payment exceptions.
- Identify records requiring duplicate checks or reconciliation.
- Monitor overdue balances and prioritize vendor follow-ups.
- Standardize recurring operational reports.
- Present key metrics through an accessible dashboard.

The workbook is a demonstration of analytical workflow and reporting design, not a validated accounting ledger or production-grade payment control system.

## Limitations & Assumptions

- The dataset is synthetic and intended for learning and portfolio demonstration.
- Duplicate flags identify potential duplicate submissions and require human review.
- The exception chart displays one assigned exception category per invoice record.
- Overdue balances are calculated from invoice amounts and successful payments; duplicate records and other reconciliation issues require review before balances are treated as final payable liabilities.
- The overdue calculation uses 14 October 2026 as the reporting date. Update the reporting date when using the workbook for a different period.

## Skills Demonstrated

Excel Data Analysis | Invoice Reconciliation | Exception Reporting | Payment Monitoring | PivotTables | PivotCharts | KPI Reporting | Dashboard Development | Finance Operations Analytics
