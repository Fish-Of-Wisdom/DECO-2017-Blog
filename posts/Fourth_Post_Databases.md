---
title: Post 4 - Databases
date: 2026-05-05
author: Sophia
summary: Diving into how SQL and databases work, and what that looks like in this project.
tags:
  - Theory
  - Databases
  - Coding
---
<link rel="stylesheet" href="assets/markdownstyle.css">

Because of the nature of the design project, we need to <span class="mint">create and handle</span> databases to store all of our information. To determine how the databases will be <span class="mint">structured</span>, what they will <span class="mint">look like</span>, and what is needed to be <span class="mint">included </span>within them, we learnt how to use wireframes to generate <span class="mint">Data Definition documents (DDD's)</span>, which can then be used to generate<span class="mint"> Entity Relationship Diagrams (ERD's)</span>. 



## DATA DEFINITION DOCUMENTS

We were directed to create <span class="mint">DDD's</span> out of every single element of <span class="mint">data</span> in our wireframes, whether we believed they were necessary in a database or not (all of the data needs to come from somewhere!)


Whenever an element called for a <span class="mint">list</span>, it was given its own <span class="mint">table</span>.

<img class="toSize" src="assets/img/ddd.png">

After completing our<span class="mint"> DDD's</span>, we needed to figure out the <span class="mint">cardinality</span> of each element - required for our <span class="mint">ERD's</span> and best worked out beforehand. 

<div class="note"><span class="note_start">!</span> I did not, in fact, work most of this out beforehand. While creating the ERD I thought through most of the relationships and the nature of their connections. While this was definitely not recommended, at least with my level of experience handling databases (basically none!), it helped to have the table fields completed and visualise connections between them after the fact. </div>





After a first pass/completing our <span class="mint">ERDS</span>, we had to decide what was <span class="mint">truly necessary</span> to be handled by a database. Things like headers and navigation bars would need to be <span class="mint">hard coded</span> as html, and therefore didn't need to be handled by a <span class="mint">database </span>/ table, whereas user replies, discussions and dropdowns would either need to, or would be <span class="mint">most optimal</span> as being stored in, a database. 

Once that was decided, we actually had to build our <span class="mint">ERD</span>! Both of us decided to complete our own versions, to better understand the process and <span class="mint">practice</span> creating them while thinking through them independently.

<img class="toSize" src="assets/img/erd.png">

<p class="note"><span class="note_start">! </span>This ERD was made using dbdiagram.io ! </p>

This is my pass at an <span class="mint">ERD</span>! It was built mostly following our <span class="mint">wireframe</span> and <span class="mint">DDD</span> of the home page, however the content on other pages would also be handled by the <span class="mint">same tables</span>, so it reflects our application as a whole.

Two tables within the<span class="mint"> ERD</span> have no connections - both dropdown menus have no bearing on the other data we need stored, and so <span class="mint">don't need</span> to be connected.

There are a few instances within the <span class="mint">ERD</span> that the <span class="mint">same</span> value is called under <span class="mint">different</span> names in different tables - most often being the <span class="mint">user id</span> given to each logged in account. This was because every table has an id column, and some hold or reference multiple types of id's - and if I was <span class="mint">specifying</span> the type of id for other values, I wanted to be <span class="mint">consistent</span> and do so across the tables - which resulted in <span class="mint">table-specific</span> field names being used instead of one, universal name. 



After creating the <span class="mint">ERD</span>, most of the planning and backend was done - the only thing left to do was actually <span class="mint">implement</span> our design. 