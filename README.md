# ServiceNow





| Feature                  | Purpose                           | Main Use Case                                       |
| ------------------------ | --------------------------------- | --------------------------------------------------- |
| ServiceNow Virtual Agent | Chatbot framework                 | Employees/customers ask questions or raise requests |
| Now Assist               | AI-powered assistant using LLMs   | Generates intelligent conversational answers        |
| Now Messenger            | Web/mobile chat widget            | Front-end chat experience for users                 |
| Agent Assist             | Helps support agents during chats | Suggests KB articles, summaries, responses          |
| Connect Agent            | Human agent communication         | Escalation from bot to human support                |




- What are the three key tables in an enterprise CMDB?
# cmdb
# cmdb_rel_ci
# cmdb_ci

ACL
Pattern.    Meaning
table.field One field
table.*.     All fields in one table
*.field.     Same field in all tables
*.*.         Everything

## Day 14 Application Scope

- Global Application
- Scope Application

* Global Application
 <p> u_ prefix
Means: custom object created in the Global scope
Example: u_vbsys_table
Created when you build something without a scoped app

👉 So:

u\_ = custom in Global scope

Global itself has no prefix for system tables:

incident
task
sys_user

But when YOU create something in Global:

ServiceNow adds u\_

- Scoped Application
  x*<company>*<app> prefix
  Means: scoped application namespace

Example:

x_vbsys_my_app
Automatically generated when you create a scoped app

👉 So:

x\_... = scoped application (correct)

| Prefix  | Meaning       | Scope      |
| ------- | ------------- | ---------- |
| `u_`    | Custom object | Global     |
| `x_...` | App namespace | Scoped app |

Simple way to remember
u* → “user-created in Global”
x* → “app-created in Scoped App”
✅ Corrected version of your statement

✔ u_vbsys → custom object in Global scope
✔ x_vbsys → part of a Scoped Application namespace

</p>

- Step Create Scope Application

* Step 1 Open ServiceNow Studio
* Step 2 Create App
* Step 3 Create Table
* Step 4 Table - Fields (Save)
* Step 5 Edit App -> Create -> Application Menu
* Step 6 Create Module - aDD TABLE
* Step 7 Open All -> Menu (Refer the VbSystem App)

* Note:
* Application = container
* Application Menu = sidebar heading
* Module = clickable link

## ✅ Updated 23-Day CSA Plan

### Day 1–10 (Same as yours)

- Why ServiceNow Needed
- Type of ServiceNow User
- User, Group & Role
- List & Form View
- Task Management
- Service-Level Agreement (SLA)
- Data Lookup Definition & Trigger Rules
- Archive Rules & Destroy Rules
- Update Set Movement
- Batch Update Set & Merge Update Set (low priority)

---

### 🔹 Core Configuration Phase

- Configuration Item & Asset Management (CMDB)
- Create Custom Table
- Form Layout & Form Design
- Application Scope & Scoped Application

---

### 🔹 Fields, Security & Logic

- Type of Fields & Enable Table Audit
- Access Control Lists (ACL)
- Application Menu & Module
- Form View & View Rule

---

### 🔹 Data Handling + Logic (UPDATED ⚠️)

- Bulk Data Load from Excel
  👉 + Import Sets & Transform Maps (MUST ADD)

---

### 🔹 Catalog & Automation (UPDATED ⚠️)

- Create Catalog Item & Workflow
  👉 + Record Producer (MUST ADD)
  👉 + Flow Designer (basic idea) (MUST ADD)

---

### 🔹 Notifications & Scripting Basics (UPDATED ⚠️)

- Email Notification
  👉 + Notification Conditions (MUST ADD)
  👉 + Business Rules (basic) (GOOD TO KNOW)
  👉 + Client Scripts (basic) (GOOD TO KNOW)

---

### 🔹 Reporting & System

- Report & Interactive Filter
- System Health & Instance Debug

---

### 🔹 ADD THIS (VERY IMPORTANT ⚠️)

👉 You didn’t explicitly include this — add it anywhere before Day 16:

🔸 UI Policy vs Data Policy (MUST ADD)

Best place: Day 15 or Day 18

---

## 🔥 Final Structure Summary

### Must-add topics now included:

✔ Flow Designer
✔ UI Policy vs Data Policy
✔ Record Producer
✔ Import Sets & Transform Maps

### Good-to-know included:

✔ Business Rules
✔ Client Scripts
✔ Notification conditions
<br>------------------------------------------<br>

- Day 11

## Configuration Item & Assets

> ⚠️ **Important Notes**
>
> # All the Assets is Configration items
>
> # All the Configuration Items is not a Asset

## How Configuration Items & Assets Created

1. Manually
2. Discovery
3. Intergration
4. Data Load via Excel Sheet

# UpdateSet - Demo

## What is UpdateSet?

- What ever configuration change done that captured in a object that object moved to one instance to another instance.

Dev (Suntec) -> Test (Suntec) -> QA (Sunted) -> Prod (FNB)

In this Demo im moving from MyDev instance -> 356655 MyTest -> 373713

---

## ServiceNow SN

### Step 1:

(SN) All -> Local UpdateSet

### Step 2:

New -> UpdateSet, New Record

### Step 3:

STRY001-RULE-RK-V1

### Step 4:

Make this myCurrentSet (click)  
STRY001-RULE-RK-V1 [What Ever i do captured in this update. Global Icon i will change red select STRY001-RULE-RK-V1]

### Step 5:

Im going to captured this change in  
(SN) All -> Assignment DataLookups

### Step 6:

New ->

- category (Inquiry | help)
- Subcategory (AntiVirus)
- Assignment Group (Help Desl)

### Step 7:

Assignment Rule if want this to captured this STRY001-RULE-RK-V1 - deActive and Save it will be saved

### Step 8:

STRY001-RULE-RK-V1 (Inprogress to changes to Complete) Save. Once Everything completed change Status.

---

### Step 9:

Move the update set From Dev -> Test

**Note:** STRY001-RULE-RK-V1; Advice not change Current UpdateSet. Always Create New updateSet STRY001-RULE-RK-V2

---

### Step 10:

From DEV -> Test Env pull the STRY001-RULE-RK-V1

### Step 11:

Test Env. (SN) All -> Update Source

- Update Source -> Dev (My Dev 356655)
- Test Env -> 373713 -> (SN) All -> Update Source

- STRY001-RULE-RK-V1 Only Completed status Moved to Test Env

---

- Test Env -> Remote Instance DEV (Setup all test Connection) -> Click, Retrieve Completed Update Sets
- Test Env -> Retrieve update set (STRY001-RULE-RK-V1) Click, Run Preview Again

- Dev -> Local Update Sets (STRY001-RULE-RK-V1) Will be Displayed
- Test -> Local Update Set (STRY001-RULE-RK-V1) will be Displayed once COMMIT UPDATE SET (Clicked). in Test -> Local Update set (STRY001-RULE-RK-V1) Displayed.

## ServiceNow Technology Stack (Now Platform)

ServiceNow is built on a proprietary technology stack known as the **Now Platform**, which follows a layered architecture composed of modern, enterprise-grade technologies.

### Core Stack

- **Programming Language:** The core backend is primarily written in Java.
- **Web Server:** The platform runs on Apache Tomcat deployed on a Linux operating system.
- **Database:** Initially built on MySQL/MariaDB, ServiceNow is transitioning toward **RaptorDB**, a high-performance database designed to support AI-intensive workloads.
- **Scripting:** JavaScript is the primary language for both client-side and server-side development, supporting modern ECMAScript standards (up to ES12).

### Architecture & Cloud

- **Infrastructure:** ServiceNow uses a **multi-instance architecture**, where each customer operates on a fully isolated instance with its own database and application logic, rather than sharing resources in a multi-tenant model.
- **Hosting:** It is a fully cloud-based platform (SaaS/PaaS). While ServiceNow manages its own global data centers, it also collaborates with hyperscalers such as Microsoft Azure and AWS for certain deployments.

### User Experience & AI

- **Frontend:** The user interface is built on the **Now Experience UI Framework**, which leverages React-inspired web components and the Seismic rendering engine.
- **Intelligence Layer:** The platform includes built-in Generative AI and machine learning capabilities through **Now Assist**, powered by domain-specific large language models (LLMs).

# Attachment

Documents attached(PDF/GIF/PNG any format) to an Incident are stored in the `sys_attachment` table.

## ServiceNow Incident Management

In ServiceNow, **Priority** and **Resolution** are distinct concepts used in Incident Management to control how quickly an issue is addressed and when it is officially closed.

- **Priority** determines the order in which incidents are handled.
- **Resolution** (tracked through the Resolution SLA) defines the time allowed to resolve the issue.

---

## SLA Customization

SLA configurations can be managed by users with the following roles:

- `admin`
- `sla_admin`
- `sla_manager`

To view or assign these roles, navigate to:  
**All → User Administration → Roles**  
(Table: `sys_user_role`)

---

## SLA Definition

To create or manage SLAs, navigate to:  
**All → Service Level Management → SLA Definitions**

---

## Learning Objectives

- Understand how to assign SLAs to users or groups
- Learn how to customize SLAs
- Learn how to create an SLA
- Understand the **SLA breach concept**:
  - If an SLA is not met, it results in a **breach**
  - This may lead to penalties based on customer agreements

# ServiceNow CSA Preparation (Xanadu Release)

This repository contains structured notes, checklists, and guidance to prepare for the  
**ServiceNow Certified System Administrator (CSA)** exam, aligned with the **Xanadu release**.

---

## ❓ Is This Enough to Clear the ServiceNow CSA Exam?

### Short Answer

⚠️ **Almost, but not fully on its own.**

---

## ✅ What This Course Covers Well

The following topics align very well with the **CSA exam syllabus (Xanadu)**:

- Users, Groups, Roles
- Lists & Forms
- Tables & Fields
- ACLs (Access Control Lists)
- Update Sets
- Import Sets / Excel Data Load
- Catalog Items & Workflow (basic)
- Notifications & Reports
- Instance Health & Debugging

👉 **Coverage:** ~**70–80%** of CSA exam content.

---

## ❌ What Is Missing or Lightly Covered

The CSA exam (Xanadu) also expects understanding of:

- Instance security concepts
  - Roles vs ACLs
  - ACL evaluation order
- CMDB fundamentals & relationships
- UI Policies vs Client Scripts
- Business Rules (when and why to use them)
- Knowledge Management
- ServiceNow best practices & governance
- Strong hands-on navigation familiarity (**critical for CSA**)

---

## 🎯 Recommendation

If you:

- ✔ Complete this course (Xanadu-based)
- ✔ Practice extensively in a **ServiceNow Personal Developer Instance (PDI)**
- ✔ Revise **CSA mock tests / practice questions**

👉 You will have an **85–90% chance of clearing the CSA exam**.

---

## 📌 CSA Xanadu Hands-On Checklist

Use this checklist to validate your readiness:

### Platform Basics

- [ ] Application Navigator & Filters
- [ ] List personalization
- [ ] Form configuration
- [ ] Saved filters

### User Administration

- [ ] Create Users
- [ ] Create Groups
- [ ] Assign Roles
- [ ] Understand role inheritance

### Tables & Fields

- [ ] Create custom tables
- [ ] Add field types (String, Choice, Reference)
- [ ] Understand table hierarchy

### Forms & UI

- [ ] Configure Form Layouts & Views
- [ ] Create UI Policies
- [ ] Compare UI Policies vs Client Scripts

### Security

- [ ] Understand ACL structure
- [ ] Create Read / Write ACLs
- [ ] Understand ACL evaluation order

### Automation

- [ ] Create Business Rules
- [ ] Identify when to use Business Rules vs UI Policies
- [ ] Basic Flow Designer understanding

### Data Management

- [ ] Import data using Import Sets
- [ ] Create Transform Maps

### CMDB

- [ ] Understand CI classes
- [ ] Create CI records
- [ ] Understand relationships

### Knowledge & Catalog

- [ ] Create Knowledge Articles
- [ ] Configure Knowledge Categories
- [ ] Create basic Catalog Items

### Reports & Notifications

- [ ] Create Reports
- [ ] Create Email Notifications

---

## 📂 Suggested GitHub Repository Structure

```text
servicenow-csa-prep/
│
├── 01-platform-basics/
│   ├── navigation.md
│   ├── lists-forms.md
│
├── 02-user-administration/
│   ├── users-groups-roles.md
│
├── 03-tables-fields/
│   ├── tables.md
│   ├── fields.md
│
├── 04-security/
│   ├── acls.md
│
├── 05-automation/
│   ├── business-rules.md
│   ├── ui-policies-vs-client-scripts.md
│
├── 06-data-management/
│   ├── import-sets.md
│
├── 07-cmdb/
│   ├── cmdb-basics.md
│
├── 08-knowledge-catalog/
│   ├── knowledge.md
│   ├── catalog.md
│
├── 09-reports-notifications/
│   ├── reports.md
│   ├── notifications.md
│
├── mock-tests/
│   ├── notes.md
│
└── README.md




 # All -> menu
 -- 1. Service Portal > Service Portal Configuration. ( Create and Configure a Portal)

# All -> users







# Study Recommendation <br>

-- Since the exam will be Yokohama release based:<br>
-- ✔ Use the latest ServiceNow University / Now Learning CSA path tied to Yokohama <br>
-- ✔ Do hands-on practice in your PDI on the Yokohama instance (or whichever latest PDI ServiceNow provides) <br>
-- ✔ Review official CSA exam blueprint for Yokohama to know exact topic weightings<br>

# URL https://dev356655.service-now.com/navpage.do




 -- 1-03-2025

 # How to Created Portal / page / Desgin (Website)

 -- Service Portal > Service Portal Configuration.
  https://dev356655.service-now.com/sp_config

 -- https://dev356655.service-now.com/$spd.do#/pm/editor/portal_meum_homepage/

 -- https://dev356655.service-now.com/sp_config (Service Portal -> Brading Editor / Design / Page Editor /Widget Editor /New Portal /Gelp Help)


 -- https://dev356655.service-now.com/$spd.do#/pm/editor/portal_meum_homepage/4a7fe71893de32507e33f9f7dd03d60e




 -- 1-04-2025
 # Service Portal Designer (SP) vs Portal Menu (PM) – Short Notes

# Service Portal Designer (SP)

-- Used to design portal pages

-- Controls layout, widgets, icons, text

-- Works on pages (e.g., sc_home)

-- Affects how the page looks and behaves

-- Page must be Active to load

-- Does not control navigation

-- Used for: UI design, widgets, page structure

# Portal Menu (PM)

--Used to manage navigation menus

--Controls menu items, links, order, visibility

--Works on menu records

--Affects how users navigate

--Menu item must be Active to appear

--Does not affect page layout

--Used for: Navigation and menu links

--Key Difference (One Line)

# SP designs pages; PM controls navigation. Both work independently and must be active as needed.

Quick Comparison Table
Feature	SP	PM
Purpose	Page design	Navigation
Widgets	Yes	No
Page layout	Yes	No
Menu links	No	Yes
Controls look	Yes	No


# Short answer (important)

-- 👉 PM itself does NOT have containers, pages, or widgets.
What you are seeing is SP content being shown through PM navigation.

-- Yes 👍 — you can change things in PM, but only certain things.
What you’re changing in PM is not the page content, it’s the navigation metadata.
That’s why it feels like you’re changing SP content.



 -- 1-05-2025

 # Simple List Widget

-- Exercise: Set Options for the Simple List Widget
In this exercise, you will set the options for the Simple List widget to display a list of active Incident records opened by the currently logged in user.

# Preparation
-- In the main ServiceNow browser window, (not the Service Portal configuration page), use the All menu to open Incident > Open.

-- Create a filter to display only active Incident records created by the currently logged in user.



# 8-01-2026

 https://dev356655.service-now.com/$spd.do#/pm/editor/portal_meum_homepage/


 # Learned

 -- Exercise: Cool Clock and the Other Widgets
 -- Exercise: Set Portal Homepage
 -- Responsive Pages

-- Fixed vs. Fluid Containers

-- Showing and Hiding Containers
-- Exercise: Hiding and Showing Containers
-- Page Editor
-- Exercise: Add a Role to a Widget
```
