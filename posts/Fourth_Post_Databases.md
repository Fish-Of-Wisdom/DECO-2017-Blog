---
title: Databases
date: 2026-05-05
author: Sophia
summary: Diving into how SQL and databases work, and what that looks like in this project.
tags:
  - Theory
  - Databases
  - Coding
---
Write your content here.

Content to include

- What we think our databases need to handle
- Setting up the DDD and ERD for our databases (from annotating wireframe)
- deciding what needs to be hard coded html vs databases (should our images be database sourced? do our nav bars need to be hard coded etc)

Because of the nature of the design project, we need to create and handle databases to store all of our information. To determine how the databases will be structures, what they will look like, adn what is needed to be included within them, we learnt how to use wireframes to generate Data Definition documents (DDD's), which can then be used to generate Entity Relationship Diagrams (ERD's). 

[IMAGE 1: PAPER FRAMES WITH ANNOTATIONS]

## DATA DEFINITION DOCUMENTS

We were directed to create DDD's out of every single element of data in our wireframes, whether we believed they were necessary in a database or not (all of the data needs to come from somewhere!)

[IMAGE: DDD EXAMPLE ON HEADER]

Whenever an element called for a list, it was given its own table.

[IMAGE: SHOW AS MANY TABLES AS YOU CAN HERE]

After completing our DDD's, we needed to figure out the cardinality of each element - required for our ERD's and best worked out beforehand. 

[IMAGE OF THIS HAPPENING]


{EXPLANATION OF WHAT IS HAPPENING}


After a first pass/completing our ERDS, we had to decide what was truly necessary to be handled by a database. Things like headers and navigation bars would need to be hard coded as html, and therefore didn't need to be handled by a database / table, whereas user replies, discussions and dropdowns would either need to, or would be most optimal as being stored in, a database. 
