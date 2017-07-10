# osbridge OCW

* General faff getting dependencies installed; see commits in repo
* Create the app on the cedar-14 stack (https://devcenter.heroku.com/articles/cedar-14-stack)

    $ heroku create --stack cedar-14 --team rcms --region eu

* Add heroku postgres add on through web interface

* Deploy the code

    $ git push heroku master

* Set `SECRET_KEY_BASE`

    $ heroku config:set SECRET_KEY_BASE="**********"

* Run database migrations and seed the DB

    $ heroku run rake db:migrate
    $ heroku run rake db:seed

* Set `OCW_APP_ROOT_URL`

    $ heroku config:set OCW_APP_ROOT_URL="https://mysterious-coast-84721.herokuapp.com"

* Upgraded from `1.0.0pre` to `1.0.0pre4` because of uninitialized constant
  error in production environment.

* Set `OCW_COMMENTS_SECRET`

    $ heroku config:set OCW_COMMENTS_SECRET="**********"
    $ heroku config:set OCW_ADMINISTRATOR_EMAIL="**********"

* Deploy new version

    $ git push heroku master

* Run database migrations and seed the DB again in case things have changed

    $ heroku run rake db:migrate
    $ heroku run rake db:seed

* Make Rails serve static assets

    # Made app change
    $ git push heroku master
    $ heroku config:set RAILS_SERVE_STATIC_FILES="enabled"

* Add OmniAuth Google OAuth2 Strategy
* Set Google keys

    $ heroku config:set GOOGLE_CLIENT_ID="**********"
    $ heroku config:set GOOGLE_CLIENT_SECRET="**********"

* Set default users as admin:

    $ heroku run console

    # List the users – I'm assuming there aren't any/many at this stage
    > pp OpenConferenceWare::User.pluck(:id, :email)

    # Update the initial users who you want as admins
    > OpenConferenceWare::User.where(:id => [2,3]).update_all(admin: true)

* Set config through ENV

    heroku config:set OCW_ORGANIZATION="Open Source Bridge"
    heroku config:set OCW_ORGANIZATION_SLUG="osb"
    heroku config:set OCW_TAGLINE="The conference for open source citizens"
    heroku config:set OCW_HAVE_ANONYMOUS_PROPOSALS=false
    heroku config:set OCW_HAVE_PROPOSAL_EXCERPTS=true
    heroku config:set OCW_HAVE_EVENT_TRACKS=true
    heroku config:set OCW_HAVE_EVENT_SESSION_TYPES=true
    heroku config:set OCW_HAVE_EVENTS_PICKER=false
    heroku config:set OCW_HAVE_MULTIPLE_PRESENTERS=true
    heroku config:set OCW_HAVE_USER_PICTURES=true
    heroku config:set OCW_HAVE_USER_PROFILES=true
    heroku config:set OCW_HAVE_EVENT_ROOMS=true
    heroku config:set OCW_HAVE_PROPOSAL_SPEAKING_EXPERIENCE=true
    heroku config:set OCW_HAVE_PROPOSAL_START_TIMES=true
    heroku config:set OCW_HAVE_PROPOSAL_STATUSES=true
    heroku config:set OCW_HAVE_EVENT_PROPOSAL_COMMENTS_AFTER_DEADLINE=true
    heroku config:set OCW_HAVE_USER_FAVORITES=true
    heroku config:set OCW_PROPOSAL_AUDIENCE_LEVEL_HINT="(Tell us the intended audience experience level for this talk)"
    heroku config:set OCW_APP_ROOT_URL="http://opensourcebridge.org/"
    heroku config:set OCW_SESSION_NOTES_URL_FORMAT="%1$swiki/%2$s/"
    heroku config:set OCW_AGREEMENT=nil

