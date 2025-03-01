# salesforce-case-automation
This repository contains a Salesforce Screen Flow-based automation for Case Management & Renewal Opportunities at Cisco Systems.

**Cisco Rapid Case Creation & Renewal Opportunity Automation**

**Overview**

This project focuses on optimizing Salesforce Case Management and Opportunity Renewal Processes for a Cisco Systems support team and sales representatives. The project consists of two primary components:

Rapid Case Creation Flow: Enables support agents to quickly log customer cases during calls.

Renewal Opportunity Creation Flow: Automates the process of cloning existing opportunity products and capturing renewal details for a streamlined sales process.

Objectives

Enhance Efficiency: Reduce manual data entry by automating case logging and opportunity renewals.

Improve Accuracy: Ensure proper assignment and status tracking using Salesforce automation.

Simplify User Experience: Use Screen Flows to guide users through form inputs and data submission.

Enable Real-Time Decision-Making: Utilize reports and dashboards for tracking case volume and renewal conversions.

Part 1: Rapid Case Creation Flow

Flow Setup: Screen Flow for Rapid Case Creation

Step 1: Create the Flow

Flow Type: Screen Flow

Flow Name: Rapid Case Creation Flow

Screen Label: "Rapid Case Creation"

Step 2: Add Screen Elements for Case Entry

Case Subject: Text Input

Case Description: Long Text Area

Status: Picklist (Dynamically Fetching Case Status values)

Priority: Picklist (Dynamically Fetching Priority values)

Origin: Picklist (Dynamically Fetching Origin values)

Assigned To: Lookup (Case Owner selection)

Step 3: Data Creation - Create Case Record

Object: Case

Field Mappings:

AccountId: Auto-populated from the recordId variable.

Subject: Mapped from screen input.

Description: Mapped from screen input.

Status: Mapped from picklist selection.

Priority: Mapped from picklist selection.

Origin: Mapped from picklist selection.

OwnerId: Mapped from lookup selection.

Step 4: Configure Quick Action to Launch the Flow

Quick Action Name: "Create New Case"

Action Type: "Launch a Flow"

Associated Flow: "Rapid Case Creation Flow"

Location: Customer Account Page for fast access by support agents.

Outcome:

Agents can quickly log cases without manually navigating multiple screens.

Cases are automatically associated with the correct Account and assigned to an agent.

Part 2: Renewal Opportunity Creation Flow

Flow Setup: Screen Flow for Renewal Opportunity Creation

**Step 1: Create the Flow**

Flow Type: Screen Flow

Flow Name: Renewal Opportunity Creation Flow

Screen Label: "Create Renewal Opportunity"

**Step 2: Add Screen Elements for Renewal Opportunity Data Entry**

Opportunity Name: Text Input

Close Date: Date Picker

Amount: Currency Input

Stage: Picklist (Fetching Opportunity Stage values)

Description: Long Text Area

**Step 3: Create Opportunity Record**

Object: Opportunity

Field Mappings:

Name: From screen input

CloseDate: From screen input

Amount: From screen input

StageName: From picklist selection

Description: From screen input

**Step 4: Retrieve & Clone Opportunity Line Items**

Get Records Element: Retrieve existing Opportunity Line Items from the original Opportunity.

Loop Through Records: Process each retrieved Opportunity Product.

Assignment: Create a new record variable for each line item.

Add Cloned Records to Collection Variable: Store all records in a collection variable.

Create Multiple Records: Batch-create all Opportunity Products for the new renewal Opportunity.

Outcome:

Sales reps can create renewal opportunities in seconds.

Product details are cloned automatically, reducing manual effort and errors.

Ensures consistent data across renewals, improving tracking and forecasting.

**Reports & Dashboards**

Key Reports:

New Cases Created Per Agent (Last 30 Days)

Average Case Resolution Time

Renewal Opportunities Created Per Sales Rep

Total Renewal Revenue (Pipeline)

Dashboard Components:

Bar Chart: Cases Created by Support Agent

Pie Chart: Case Status Distribution

Gauge: Opportunity Renewal Performance

Table: Top Renewal Deals

**Key Takeaways**

✅ Optimized Salesforce case logging via Rapid Case Creation Flow.✅ Automated renewal pipeline for sales reps, improving efficiency.✅ Seamless experience for agents & sales teams using guided screen flows.✅ Real-time reporting and dashboards for monitoring support & sales trends.✅ Improved accuracy and compliance with pre-configured automation rules.

**Next Steps**

Implement validation rules to prevent duplicate cases.

Set up email alerts for case assignments and renewals.

Expand reporting to track case resolution time against SLAs.

Further optimize the UI for better case tracking visibility.

This project enhances Salesforce's Case Management & Opportunity Renewal capabilities, helping businesses improve customer support efficiency and sales performance with automation and data insights.
