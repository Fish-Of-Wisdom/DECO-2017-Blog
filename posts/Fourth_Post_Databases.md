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
<link rel="stylesheet" href="assets/markdownstyle.css">

Because of the nature of the design project, we need to create and handle databases to store all of our information. To determine how the databases will be structures, what they will look like, adn what is needed to be included within them, we learnt how to use wireframes to generate Data Definition documents (DDD's), which can then be used to generate Entity Relationship Diagrams (ERD's). 

[IMAGE 1: PAPER FRAMES WITH ANNOTATIONS]

## DATA DEFINITION DOCUMENTS

We were directed to create DDD's out of every single element of data in our wireframes, whether we believed they were necessary in a database or not (all of the data needs to come from somewhere!)

[IMAGE: DDD EXAMPLE ON HEADER]

Whenever an element called for a list, it was given its own table.

<img class="toSize" src="assets/img/ddd.png">

After completing our DDD's, we needed to figure out the cardinality of each element - required for our ERD's and best worked out beforehand. 

<div class="note"><span class="note_start">!</span> I did not, in fact, work most of this out beforehand. While creating the ERD I thought through most of the relationships and the nature of their connections. While this was definitely not recommended, at least with my level of experience handling databases (basically none!), it helped to have the table fields completed and visualise connections between them after the fact. </div>





After a first pass/completing our ERDS, we had to decide what was truly necessary to be handled by a database. Things like headers and navigation bars would need to be hard coded as html, and therefore didn't need to be handled by a database / table, whereas user replies, discussions and dropdowns would either need to, or would be most optimal as being stored in, a database. 

Once that was decided, we actually had to build our ERD! Both of us decided to complete our own versions, to better understand the process and practice creating them while thinking through them independently.

<img class="toSize" src="assets/img/erd.png">

This is my pass at an ERD! It was built mostly following our wireframe and DDD of the home page, however the content on other pages would also be handled by the same tables, so it reflects our application as a whole.

Two tables within the ERD have no connections - both dropdown menus have no bearing on the other data we need stored, and so don't need to be connected.

There are a few instances within the ERD that the same value is called under different names in different tables - most often being the user id given to each logged in account. This was because every table has an id column, and some hold or reference multiple types of id's - and if I was specifying the type of id for other values, I wanted to be consistent and do so across the tables - which resulted in table-specific field names being used instead of one, universal name. 

<p class="note"><span class="note_start">! </span>This ERD was made using dbdiagram.io ! </p>

After creating the ERD, most of the planning and backend was done - the only thing left to do was actually implement our design. 