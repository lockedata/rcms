Central Admin Issues (and related conference admin issues)
================

## Create user/conference account

    Create accounts for people and assign them the role of conference admin

It is possible for an admin to create user or admin accounts on all
systems. None of the systems send invitation emails automatically
(though Odoo should).

Specific details:

  - **Oconf** Users can only sign up via a Google account in test
    system, but other options (OpenID, custom form) should be possible.
    Users can be made admins in order to manage accounts and events.

  - **Osem** Users can sign up via web form. Users can be made admins
    (right to create a new conference, manage users and make other users
    admins) or organizers of a specific event.

  - **Odoo** User/admin accounts must be created by an admin. Access
    rights are applied to whole categories (e.g. “events”, “website”,
    “administration”) so it’s not clear that we could restrict access
    rights to a specific event. It seems there is an add-on for user
    sign-up: <https://apps.odoo.com/apps/7.0/auth_signup/>.

Overall: All systems usable, but due to control over access rights and
ease of signing up, OSEM \> Oconf \>
    Odoo.

## Create and brand a conference template

    Create a conference template for a set of events. Apply things like logos and branding.

It is not possible to create a conference template on any of the
systems, but Odoo allows you to create an event based on a previous one,
which amounts to much the same thing.

Specific details:

  - **Oconf** Each event must be created from scratch. It is not
    possible to group events by type (e.g. to separate satRdays and
    useR\!s).

  - **osem** Each event must be created from scratch. There is a custom
    name for the whole site (R Conferences), so it would be possible to
    have separate instances for useR\! and satRdays with their own
    branding. But then we might lose the benefit of a common log in and
    user profile.

  - **odoo** An event can be created from a previous event, carrying
    forward any customisations (e.g. changes to the default website).
    The website is branded by the organizing “company”, so it would be
    easiest to have separate instances for satRdays and useR\!. However
    the website appears to be fully customizable, so with a bit more
    work we could create one website for all, with separate info pages
    for satRdays and R Foundation conferences (or each conference
    series). Events are tagged by organizer and type, so this would help
    to differentiate conference series if required.

Overall: All systems can be used for multiple events, but Odoo is most
suited to running repeat events (with minimal effort) and different
(branded) conference
    series.

## Create a new conference

    Setup a new conference page. If possible, use a template you created.

It is possible to create a new conference on all systems. On Oconf and
OSEM this must be done from scratch, on odoo it can be based on a
previous event.

  - **oconf** The assumption is that this is a page for proposals, not a
    general conference website. You have to create a proposal deadline,
    but this does not appear anywhere on the page. The time zone of the
    deadline is unspecified. You have to create a Track and a Session
    type otherwise you get warnings. The tracks/sessions are not shown
    to the user on the proposal submission form. A lot of the content on
    the conference page is hard-coded, e.g. adding “proposals” to the
    page title. It does not seem possible to add a logo/branding. It is
    possible to use HTML in the editing text boxes, which gives some
    control over formatting. Perhaps this would allow logos to be added
    but this would require more systems admin to load the image files
    somewhere.

  - **osem** A conference page is created by adding a new conference to
    the system specifying the name and dates of the conference, then
    adding a splashpage in the basics menu. This uses a default
    template. I tried to upload a logo (png) but it doesn’t seem to find
    it - I guess this needs to be put on the server. You cannot delete a
    conference from the CMS, only from the rails console (conferences
    are hidden once date has passed).

  - **odoo** Creating an event is a bit unintuitive. The “Location” is
    either an individual or a company and their address determines the
    location of the event. The “Organizer” is a company, so should be
    satRdays or useR\! local committee or similar (even though satRdays
    is the only company in the settings, I could add another company as
    an organizer for a particular event). A default webpage is created,
    but this is fully customisable. An event can be duplicated to form
    the basis of a new one.

Overall: Only OSEM and Odoo have potential to form a full conference
website.

# Customise conference content

``` 
Customise the conference page made for you by the central admin: 
 - Add content
 - Create additional pages / content locations
 - Tweak style if required
 
```

The ability to customise varies by CMS.

Specific details:

  - **osem** You can modify the basic information (dates, venue etc). I
    don’t see a way to create additional pages/sections. At the moment
    there doesn’t seem to be a good place to put e.g. travel
    information, code of conduct, FAQ. There is limited ability to tweak
    the style (base colour). Some aspects of the page seem to be
    hard-coded, e.g. “useR2019 has the most awesome program ever\! See
    rock-star speakers cover the topics of” and “Don’t miss out\!”.

  - **oconf** There is not much capacity for customisation. The Snippets
    menu contains a “proposals\_form\_text” item which is not the same
    as the text on the proposal form, so not clear how we would edit
    that.

  - **odoo** There is a WSIWYG editor to add pages and sections. The
    dates are in US format: the WSIWYG editor appeared to allow me to
    change the date text but it didn’t save. It appears you can write
    your own website templates using Python
    <https://www.odoo.com/documentation/11.0/howtos/website.html> but
    this would be much more involved.

Overall: In terms of ability to customise Odoo \> OSEM \> Oconf. Only
Odoo has the potential to hold all the information about the conference,
but we might need to develop a template in Python for all the features
we would need. Oconf may be okay as a site for managing abstract
submission.

# Configure conference

``` 
 - Provide key info like dates and location
 - Add team members who need access to the system
 
```

All CMS allow to set date and location.

  - **oconf** You can set the dates but these don’t automatically appear
    in the conference webpage. Location needs to be added in custom
    text.

  - **osem** I updated the name and date via the Basics dialog and the
    place/country via the Venue dialog. It is only possible to add
    video/photo for the venue from certain providers (YouTube,
    Instagram, Flickr, SlideShare, SpeakerDeck). I edited the contact
    email and Twitter account. You can’t create a mailto link, so you
    can’t use this to add subject filters to queries, e.g. for sponsor
    contacts (it allows you to add a separate address for this).

  - **odoo** Dates and location can be set when the event is created. As
    mentioned, the dates are in US format. This
    <https://www.slideshare.net/deepsvirzoteck/change-date-format-in-odoo>
    suggests it may be possible to change to other formats if you have
    Settings administration rights (I only have Access Rights).

Overall: only Odoo and OSEM link setting the dates and location to the
conference website, but both are constrained in how this is displayed.

# Conclusions based on these issues

Oconf is designed to manage proposal submission and conference schedule.
It is not suitable for creating a conference website with all essential
information.

OSEM can create a basic conference homepage, but hard-codes things we
wouldn’t want and does not have capacity to add essential information,
e.g. travel info. We would need to contribute to/fork the OSEM project
to extend, as this is a Ruby on Rails app, this would require skills
that may be hard to find within R community. The devel version has
removed some of the hard-coding, but is unstable and we still may need
to fork to add pages/ customize as we need.

Odoo has the potential to create a full conference site and has the
benefit of easy duplication to create a new event. Some issues,
e.g. user sign up, date format, may be fixable with full admin rights
or by adding apps to the installation. It is possible we may need to
develop a Python template to get everything as we would like, but
knowledge of Python is more common in the R community.

# Other alternatives

[Hoverboard](https://github.com/gdg-x/hoverboard) mentioned by Natalie,
looks somewhat like OSEM but more customisable. It is designed to create
a single conference website (all the above create a hub for multiple
events). Editing would be more low level, but perhaps more accessible to
R users (blog posts written in markdown, page templates in Javascript).
Seems to be templates for most standard content: overview, featured
speakers (randomly selected from all), google map of location, space for
partners. Nice-looking schedule: example with 6 parallel sessions:
<https://valleydevfest.com/schedule/>, tabs for multi-day schedules.
Possible to save sessions, but can’t try without signing in. Nice
speaker profiles. Mobile friendly. Offline access. Additional content
e.g. CfP can be added as blog posts. Tickets and CFP links go to
external sites.

<https://conf.researchr.org/> used by Jan. Main hub covers mostly ACM
conferences, so would not (by default) have hub for R conferences. Users
can sign up to conf.researchr.org system from a single conference site.
Template for single conference contains ability to add custom pages
e.g. for travel scholarship, banquet info etc. Design fairly plain but
can add conference banner and photos to customise. Sponsor layout does
not seem to allow bigger logos for bigger sponsors. Timetable design not
fancy but good level of detail. Can star events and add to personal
program. Nice speaker bios. Need contract with HotCRP ($7.50 per
submission) or Conference Pubmishing Consulting?? in order to batch
upload abstracts, so not ideal. Not sure if this is a free service, not
open source.

[user\! 2018 page](https://github.com/useR-2018/website) this is a basic
Hugo website. The main site has all the essential info with the ability
to add custom section/pages as required. Since the content is all in
markdown this would be most simple for useRs to modify and update. New
conferences can be created by cloning the GitHub repo and modifying. The
style could be updated/customised for a different series by updating the
HUGO templates, again with the popularity of blogdown, many useRs have
experience of this. If the “all-in-one” options do not meet other
requirements for selling tickets and/or managing abstracts, this could
be the simplest and most customisable solution, however we would
probably need external service for a timetable tool. This is affordable
for useR\! and not so important/unnecessary for satRdays, but an
unwanted expense for other conferences we may wish to support (also
Sched has its own issues regarding usability).

Hoverboard may provide alternative if one-for-all solutions do not work
out. Accessibility should be taken into account before a final decision
is made.
