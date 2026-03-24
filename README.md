# ServiceNow


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