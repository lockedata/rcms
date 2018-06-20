# Project update: Revised strategy and project plan
After making the [findings report](./cms_evaluation_report.md) and [presentation](https://1drv.ms/p/s!AiZm2P6YHtSfg4lpg8XOz0ThAGdGhg) available for review, we met today to review the results of the R Conference Management System project’s system evaluation phase.

Odoo was identified as the most feature-rich platform for hosting events out of three that went through an in-depth assessment. However, the following issues were noted:
-	Due to the general-purpose nature of Odoo, it was difficult to identify what was needed to be done with respect to managing events
-	Odoo’s workflow for talk submissions, review, and selection was not flexible and was inadequate for UseR! Needs

We discussed the option of extending Odoo as it was based on Python, but it was felt that trying to make a one size fits all solution was not the best approach.

The alternative we discussed and will now move forward with is a flexible and minimal solution in Hugo, the basis for blogdown.
Hugo is a static site generator that use templates to build sites from markdown or JSON and CSV datasets. It is widely adopted in the R community and requires mostly HTML and CSS skills for development.

We also discussed the state of the annual UseR! events. The 2019 event is planning on using the [sciencesconf.org](https://sciencesconf.org) system for delivering their event so no major technical requirements are currently needed until the 2020 event which isn't likely to need work for the next year. The use of the satRdays with the more numerous events will allow rapid iteration and refinement of the integrations over the next year. This  will mean other R events can leverage the solutions developed for satRdays and the technology will be proven by the next UseR! iteration.

In terms of how this translates to a revised milestone plan. The original was Milestone 3 Development (USD$13,000) and Milestone 4 Production (USD$3,750). We propose a new structure with the two events milestone's running in parallel:

## SatRdays (USD$11,000)
1. (USD$3,000) The development of a satRdays conference template theme
2. (USD$6,000) The development of some templates for consuming some key systems, APIs, and datasets for attendee registration, call for speakers, and schedules used by satRdays so far
3. (USD$2,000) Supporting the use of the initial template theme and integrations in a satRdays event and providing video training and documentation on the tools 

## UseR! (USD$5,750)
4. (USD$1,000) A style guide and mockup of a UseR! Conference page that could be used for customising the look and feel of the 2019 site in sciencesconf and used more heavily in the 2020 conference
5. (USD$4,750) The development of a Proof of Concept custom CFP workflow based off a previous UseR! Iteration involving Redmine that can be implemented when organisers do not feel existing solutions fit their needs

These smaller deliverables will make up the remainder of the project, and the custom CFP system is likely to be performed by Open Analytics, the organisation who supported the UseR! build previously.

