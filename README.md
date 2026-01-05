# ServiceNow



 # All -> menu
 -- 1. Service Portal > Service Portal Configuration. ( Create and Configure a Portal)







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