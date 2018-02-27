# R CMS evaluation results 
| Functionality                          | Odoo        | Osem        | Oconf       |
|----------------------------------------|-------------|-------------|-------------|
| [Manage registration](#manage-registration)                    | fail        | success     | fail        |
| [Register](#register)                               | fail        | fail        | fail        |
| [Build agenda](#build-agenda)                           | success     | success     | success     |
| [Submit talks](#submit-talks)                           | fail        | fail        | fail        |
| [Manage attendees](#manage-attendees)                       | in progress | in progress | in progress |
| [Manage sponsors](#manage-sponsors)                        | in progress | in progress | fail        |
| [Manage speaker submission](#manage-speaker-submission)              | in progress | in progress | in progress |
| [Setup session submission](#setup-session-submission)              | fail        | fail        | fail        |
| [Setup tickets](#setup-tickets)                          | success     | fail        | fail        |
| [Configure conference](#configure-conference)                   | success     | success     | success    |
| [Customise conference content](#customise-conference-content)           | success     | fail        | fail        |
| [Create a new conference](#create-a-new-conference) | success     | success     | success     |
| [Create and brand a conference template](#create-and-brand-a-conference-template) | success     | fail        | fail        |
| [Create user/conference accoun](#create-user/conference-account)         | success     | success     | success     |


With 3 tasks still pending, Odoo has had the most successful evaluations of critical tasks, with osem and then oconf having fewer successes.

## Manage registration
Issues 46,45,44
### Comments from evaluator [@tvedebrink](https://github.com/tvedebrink)
- **Odoo**- I can't login on the satuRday pages.
- **Osem**
    + Profile update went fine 
    + For the refund, the website prompts: *"Your ticket purchases won't be refunded. Are you sure you want to unregister?"*
- **Oconf**
    + Edit of profile went fine  
    + Cant manage to buy tickets - hence no refund possible

### Notes / synopsis
Registration management for attendees is important unless we were to rely on a manula/ back office option. 


## Register
Issues 43,42,41 

### Comments from evaluator [@tvedebrink](https://github.com/tvedebrink)

- **Odoo**- I can't login as I don't know how to sign up a new account
- **Osem**
    + I "bought" a free ticket to the event. I haven't tried to pay for one.. 
    + I couldn't print or retrieve my ticket (neither using show or pdf)
- **Oconf**- I can't find the link or formula to buy a ticket for the event

### Notes / synopsis
This is a serious blocker.

- TODO: [@amymcdougall](https://github.com/Amymcdougall)  see if you can register for an event on odoo under a dummy email address
- TODO:  [@amymcdougall](https://github.com/Amymcdougall)  see if you can register for an event on oconf 

## Build agenda
Issues 40,39,38 
### Comments from evaluator [@tuxette](https://github.com/tuxette)
- **Odoo**- I managed to create rooms, sessions and to assign speakers to sessions (not papers though: you can only have the session title and the speaker name but not the title of the talk). I was also able to define different types of sessions and to publish the program.
- **Osem** Once the events (actually an event = a talk or a session) have been defined and accepted it is easy to arrange them into a program. The main difficulty seems to be that I think we cannot really put session and talks into the program: you can define a session, in the "abstract" of the session write the details about the different talks or if you define the event at a talk level you won't be able to arrange them into sessions.
- **Oconf** - I managed to create rooms, session and to publish a program. However, I am not sure if we can easily affect submissions to sessions for instance. Maybe this has to be done manually.

### Notes / synopsis
It looks like (limited) success was had with each system. 

- TODO: [@amymcdougall](https://github.com/Amymcdougall) see if there's options we missed that would facilitate a better experience on each of these systems?
## Submit talks
Issues 37,36,35
### Comments from evaluator [@Tvede](https://github.com/tvede)
**Odoo** - Don't know how to create an account?
 **Osem** - I could register for the conference.  
 I couldn't generate a pdf with my registration details.
 I can't figure out how to submit a talk..
 **Oconf** - I was able to sign-in/login on the oconf site using my google account (but not by other means??)
I coundn't submit a session proposal.
## Manage attendees
Issues 34,33,32
### Comments from evaluator @juliejosse
**Odoo** *IN PROGRESS- @juliejosse*
**Osem** - *IN PROGRESS- @juliejosse*
**Oconf** - *IN PROGRESS- @juliejosse*
## Manage sponsors
Issues 31,30,29 
### Comments from evaluator @juliejosse
**Odoo** *IN PROGRESS- @juliejosse*
**Osem** - *IN PROGRESS- @juliejosse*
**Oconf** - For now, I have a message: "something went wrong..."
## Manage speaker submission
Issues 28,27,26
### Comments from evaluator [@thothorn](https://github.com/thothorn)
**Odoo** - *IN PROGRESS- [@thothorn](https://github.com/thothorn)*
**Osem** - *IN PROGRESS- [@thothorn](https://github.com/thothorn)*
**Oconf** - *IN PROGRESS- [@thothorn](https://github.com/thothorn)*

### Notes / synopsis
[@thothorn](https://github.com/thothorn) had emailed and is confused on what the tasks are asking him to do

## Setup session submission
Issues 25,24,23
### Comments from evaluator [@tuxette](https://github.com/tuxette)
**Odoo** - I haven't seen anything about paper submission in this system...
**Osem** - I was able to define tracks and event types (almost: length has to be a multiple of at least 5 minutes which can be a problem for lightning talks?)  
but  I was not able to configure CFP. I do not have the proper rights it seems (because it worked well on OSEM Demo).
In conclusion:  
(ðŸ‘) Define any tracks / categories required  
(ðŸ‘Ž) Configure CFP details  
(ðŸ‘Ž) Add CFP content like FAQs  
(ðŸ‘Ž) Customise form
**Oconf** - (ðŸ‘) Define any tracks / categories required  
(unsure) Configure CFP details (maybe I did it but I was not able to check: I did not find where it appears on the public website  
(ðŸ‘Ž) Add CFP content like FAQs  
(ðŸ‘Ž) Customise form (did not find where to do that)
## Setup tickets
Issues 22,21,20

**Odoo** - ðŸ‘ Create tickets for the conference  
ðŸ‘Ž Add a payment provider (I think that the functionality exists in "Sales". However, the framework is so different from a conference that I am not able to see where and how)  
ðŸ‘ Customise registration form (to a certain extent: text questions are limited to Name, Email and Phone, Address, Country. Maybe affiliation (at least) would be useful). Also for multiple option tickets (ex: registration + gala), some parts of the form has to be filled twice...!  
ðŸ‘ Customise confirmation email (very well made)
**Osem** - (ðŸ‘) Create tickets for the conference (except that once the currency is set, you cannot change it)  
(ðŸ‘Ž ) Add a payment provider (I did not find where to add payment provider)  
(ðŸ‘Ž) Customise registration form (I was able to add questions but not to change the registration dates nor to display the registration form)  
(ðŸ‘) Customise confirmation email (I think that is done properly)
Just adding to Nathalie's comments: I also tried to play around with the currencies. Inconvenient that once these are set they cannot be changed (apparently only deleted). Also you cannot mix currencies.
**Oconf** - I found no information about how to configure a registration...
*(issues 22,21,20 - [@tuxette](https://github.com/tuxette)*

### Notes / synopsis*Note: extra comment form [@statibk](https://github.com/statibk)

## Configure conference
Issues 19,18,17
### Comments from evaluator [@tuxette](https://github.com/tuxette), [statibk](https://github.com/statibk) & [hturner](https://github.com/hturner) had input also.
**Odoo** - Can provide key info like dates and location  
Can add team members who need access to the system *[@tuxette](https://github.com/tuxette)*
**Osem** I updated the name and date via the Basics dialog and the place/country via the Venue dialog. It is only possible to add video/photo for the venue from certain providers (YouTube, Instagram, Flickr, SlideShare, SpeakerDeck). Some aspects of the page seem to be hard-coded, e.g. "useR2019 has the most awesome program ever! See rock-star speakers cover the topics of" and "Don't miss out!".
I tried to upload a logo (png) but it doesn't seem to find it - I guess this needs to be put on the server.
I edited the contact email and Twitter account. You can't create a mailto link, so you can't use this to add subject filters to queries, e.g. for sponsor contacts (it allows you to add a separate address for this).  *[hturner](https://github.com/hturner)*
ðŸ‘ *[@tuxette](https://github.com/tuxette)*
ðŸ‘ Modified a few things (dates, colors, etc.) which worked ok. *[statibk](https://github.com/statibk)*
**Oconf** -  (unsure) Provide key info like dates and location (date is set properly but I am unsure if I am using well the system to describe the conference)  
(thumbs up) Add team members who need access to the system *[@tuxette](https://github.com/tuxette)*
## Customise conference content
Issues 16,15,14
### Comments from evaluator [@tuxette](https://github.com/tuxette) & [hturner](https://github.com/hturner)
**Odoo** - ðŸ‘ Add content  
ðŸ‘ Create additional pages / content locations  
ðŸ‘ Tweak style if required (manageable but not super easy: I had problems to insert HTML code for instance)  *[@tuxette](https://github.com/tuxette)*
Just noticed dates are in US format. This  [https://www.slideshare.net/deepsvirzoteck/change-date-format-in-odoo](https://www.slideshare.net/deepsvirzoteck/change-date-format-in-odoo)  suggests it may be possible to change to other formats if you have Settings administration rights (I only have Access Rights). The WSIWYG editor appeared to allow me to change the date text but it didn't save.
It appears you can write your own website templates using Python  [https://www.odoo.com/documentation/11.0/howtos/website.html](https://www.odoo.com/documentation/11.0/howtos/website.html)  but this would be much more involved.  *[hturner](https://github.com/hturner) had input also.)*
**Osem** - You can modify the basic information (dates, venue etc).
I don't see a way to create additional pages/sections. At the moment there doesn't seem to be a good place to put e.g. travel information, code of conduct, FAQ.
There is limited ability to tweak the style (base colour). *[hturner](https://github.com/hturner)*
same comment than Heather: I am able to change basic things like conference dates and venue but I don't see where to add additional pages. Customization of the pages does not seem very easy to do (no WSIWYG editor) and the website template seems to be more or less fixed.  *[@tuxette](https://github.com/tuxette)*
**Oconf** - Can't add content  
Can't create additional pages / content locations  
Can't t weak style if required  
I was not able to find anywhere where to customise the website look or content.
## Create a new conference
Issues 13,12,11
### Comments from evaluator [hturner](https://github.com/hturner)
**Odoo** - You can't create a conference template as such, but you can duplicate an event and edit it, which makes creation of new events much easier. So I both created a new conference from scratch and a conference based on a previous one, see [#10](https://github.com/lockedata/rcms/issues/10) for further comments.
**Osem** - It is easy to create a new conference page, but it does not seem to be possible to create a conference template or to create a new conference based on an existing one.
**Oconf** - I created a web page for useR! 2020 from scratch - it does not seem possible to use a template.
As mentioned in  [#8](https://github.com/lockedata/rcms/issues/8)  the assumption is that this is a page for proposals, not a general conference website. You have to create a proposal deadline, but this does not appear anywhere on the page. The time zone of the deadline is unspecified. You have to create a Track and a Session type otherwise you get warnings (which get replicated if you reload the page!). The track "useR! 2020 Talks" is visible to the user in the legend of the schedule - which is empty at present. The tracks/sessions are not shown to the user on the proposal submission form. It's not clear how we might edit this form - the Snippets menu contains a "proposals\_form\_text" item which is not the same as the text on the proposal form.
It is possible to use HTML in the editing text boxes, which gives some control over formatting. Perhaps this would allow logos to be added but this would require more systems admin to load the image files somewhere.
## Create and brand a conference template
issues 10,9,8
### Comments from evaluator [hturner](https://github.com/hturner)
**Odoo** - This interface was the least intuitive and the docs are hopeless, but this looks much more powerful.
The website is designed as if it hosted by a company that runs events. So the simplest way to adopt it would be to have separate instances with satRdays as the company in one case and the R Foundation as the company in the other. However the website appears to be fully customizable, so with a bit more work we could create one website for all, with separate info pages for satRdays and R Foundation conferences (or each conference series). Events are tagged by organizer and type, so this would help to differentiate conference series if required.
Currently satRdays is registered as a company in the settings. I could not add "useR! conferences" as a separate company. I could change satRdays to useR!, but I reverted this change as other content has already been added about satRdays. The company settings produce some default content on the webpage, e.g. overall site logo, but this is customisable.
Creating an event is a bit weird. The "Location" is either an individual or a company and their address determines the location of the event. The "Organizer" is a company, so should be satRdays or useR! local committee or similar (even though satRdays is the only company in the settings, I could add another company as an organizer for a particular event). There seem to be a large number of irrelevant in-built options, which is a bit distracting, maybe we could delete those. Sometimes clicking "Edit" does not seem to be enough, for example I didn't set the start and end times to begin with, in order to change this I had to click "Edit" and then "Set to draft".
However once you work out how to create and edit the event a nice default webpage is created. This is fully customisable. If I add a section (e.g. for one event I created a few spots to advertise the keynote speakers) and then duplicate the event to form the basis of a new one, the customisation gets carried forward. This means it is much easier to create a similar event the next time.
**osem** - It does not seem to be possible to create a conference template or an umbrella page for a set of events.
The system does have a custom name for the whole site (R Conferences), so it would be possible to have separate instances for useR! and satRdays with their own branding. But then we might lose the benefit of a common log in and user profile.
**Oconf** - I tried to create a page for all useR! events, how it is only possible to create an event page. A lot of the content on this page is hard-coded, e.g. adding "proposals" to the page title. It does not seem possible to add a logo/branding. The events menu shows the name of the currently selected event, which is confusing, e.g. when I am on the useR! page, the events menu button is named "useR" with options "useR" and "sample conf".
I then tried to create a page for useR! 2019 as a child of the useR! page. This is possible, but then I can't navigate to the useR! 2019 page from the navigation bar! (It shows on the /events/ page).
So I gave up on creating a set of events and created a stand-alone page for useR! 2020. (See issue  [#11](https://github.com/lockedata/rcms/issues/11)).
Overall this is looking like an abstract handling site, not a conference management site.
## Create user/conference account
Issues 7,6,5
### Comments from evaluator [hturner](https://github.com/hturner)
**Odoo** - I set up an account for Natalie with access rights, so hopefully she has the editing permissions she needs. I could not send an invitation email though. (Also I accidentally hit "Inactive" when creating the record, so Natalie was not in the default User view - changing the filter to include inactive users fixed this and it was easy to activate the account). The access rights are applied to whole categories (e.g. "events", "website", "administration") so it's not clear that we could restrict access rights to a specific event. This might require a bit more effort to keep on top of, in particular revoking access for organizers of past conferences.
**Osem** - I added Achim as a user and made him an admin via the checkbox in the user profile. This gives him the right to create a new conference, manage users and make other users admins. You can only see that he is an admin from the Edit user page (it doesn't seem to show as a Role).
I added Nathalie as a user and made her an organizer of the "useR2019" conference. This should give her full access to that conference.
**Oconf** - I signed up as a user and Steph made me an admin. It's currently only possible to sign in with a Google account, this is nice to have as an option but it should not be the only option.
I also made Nathalie an admin after she had signed up as a user. There were the options
-   Admin?
-   Selection committee?
-   Complete profile?
and I selected only admin (could choose any combination by the look of it).
*(issues 7,6,5 [hturner](https://github.com/hturner))*
