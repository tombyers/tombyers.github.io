---
title: Reducing the cost of experimentation
date: 2020-04-19 10:46:00 Z
---

The end product of designing a form often looks simple and somehow inevitable, but the process of designing one well is far from straightforward. And while forms aren't a trendy part of digital experiences, they're a central component of most digital tools we use.

The trouble in designing forms is the sheer number of decisions involved.

**Context**

* What information do we need?
* What will it be used for? Who by?
* Where does this information exist? Do we need someone to enter it or can we get it from somewhere already?

**End user**

* Who will enter the information?

* In what context?

* Do they have the information? If not, where will they find it? 

**Content**

* How should we ask for this information?
* What language should we use? Will the terms we choose mean the same thing to everyone?
* What options do we give e.g. in checkbox lists and dropdowns? Is it clear what these mean? Do they cover everything? Are there too many to process? What should the user do if they don't know?

**Interaction design**

* How can we make it fast and simple to fill in the information?
* Can we provide sensible default values?
* If someone enters something incorrectly, how do we help them correct it?

At Sensyne Health, I worked on the user experience design for midwives and doctors using GDm-Health, a product to remotely monitor the blood sugar levels and medications of pregnant women with gestational diabetes. During clinic appointments, doctors and nurses would review a woman's blood sugar chart and update her pregnancy notes and medical records in GDm-Health.

As described earlier, the difficulty with form design is the huge number of possible variants and the number of decisions to make. My solution to this - at least to address the interaction design level decisions - was to **reduce the cost of making decisions**. This meant making it as easy and effortless as possible to change the way the form pages were designed.

We use Sketch for design work at Sensyne Health. I like Sketch. But it's of a limited use for designing forms. The mock-ups you create in Sketch are static, not interactive. Setting up complex clickable prototypes is slow, as is testing detailed interactions. And interactivity aside, simply changing decisions mid-design is slow. If I decide to change one form element from a dropdown list to a list of radio buttons, perhaps across a few artboards, I need to go and tidy-up the spaces I messed with manually.

I decided to create a code-based prototype. It would be live and accessible on the web - easy to share with the product and engineering teams. And critically, it would be easy to re-configure. If I wanted to change how form questions were presented, I could do that simply; everything would *just work.*

I hooked React components up to a long JSON file that simply described the form I wanted, listing field by field the information and the type of form element used for each.