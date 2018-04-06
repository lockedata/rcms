# Evaluating existing open source conference management tools

## High-level results
We have completed the evaluation of the conference management solutions shortlist to identify which one met requirements the best. Based on the evaluation, Odoo is by far the strongest solution. 

In terms of implementation, we would require an Odoo instance per organisation (satRdays, UseR!, etc) for ease and then setup dummy events that can be used for templates, but Odoo system creation is very easy. 

The greatest area of weakness was the call for papers facilities, especially for events looking to use an academic conference workflow.
It also became clear that some stakeholders were not happy with a single solution, preferring to use their own multi-system stacks. Given a lack of ideal fit in a key workflow and somem resistance to a single solution, **the decision arising from this evaluation is whether Odoo should be adopted or something like an integration framework should be investigated.**


## Evaluation results
The original list of candidates were reviewed based on documentation and demo sites.

|               | Conf Page | Call for Papers | Tickets | Agenda | Users | Notes |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| **OCS** | Old, unsupported, requires server installation, not visually customisable, looks like a Win 95 app | N | Y | Y | Y | N | 
| **Indico** | Demo failed badly, very hard to access, *assumed (couldn't access in demo), **Uses Cern central login, extremely hard to use and unstable | Y | Y | Y | Y* | Y** | 
| **Frab** | Barebones, still in beta (5 years+), ticketing only via external services | Y | Y | N | Y | Y |
| **OSEM** | Fully customisable, single page website design, very modern, fully open (via GitHub), web based (css, yml, md, html), easy to use | Y | Y | Y | Y | Y |
| **Odoo (Events)** | Big ERP open source solution, easy setup, self-contained service, professional and modern appearance, full site design, web access, has a SAAS version but we can get a community edition using our own server. Has blog, chat, spreadsheet, event management, e-commerce, POS service (so very powerful!)  | Y | Y | Y | Y | Y |
| **OCW** | Heavy duty, low documentation, depends on Ruby on Rails, additional features such as external account login (i.e. Facebook),  less customisable, more toggleable| Y | Y | Y | Y | Y |

Based on these results, OSEM, OCS, and Odoo were shortlisted for in-depth evaluation. High-level results arer outlined below, but in-depth commentary can be found at [evaluation notes](reviews/rcms_review(am).md).

| Functionality                          | Odoo        | Osem        | Oconf       |
|----------------------------------------|:-----------:|:-----------:|:-----------:|
| Manage registration                    | fail        | success     | fail        |
| Register                               | success     | fail        | fail        |
| Build agenda                           | success     | success     | success     |
| Submit talks                           | success     | success     | fail        |
| Manage attendees                       | in progress | in progress | in progress |
| Manage sponsors                        | in progress | in progress | fail        |
| Manage speaker submission              | in progress | in progress | in progress |
| Setup session submission               | fail        | fail        | fail        |
| Setup tickets                          | success     | fail        | fail        |
| Configure conference                   | success     | success     | success    |
| Customise conference content           | success     | fail        | fail        |
| Create a new conference                | success     | success     | success     |
| Create and brand a conference template | success     | fail        | fail        |
| Create user/conference account         | success     | success     | success     |

