# Making admins
1. To make someone an admin note their user id - find it at url mysterious-coast-84721.herokuapp.com/users
2. Open a cmd line to the app location e.g. `heroku > more > open console`  or `ssh heroku && cd /app/root`
3. Provide `console` as the input to the heroku console or run the line `bin/rails console`
4. Run `OpenConferenceWare::User.find(USER_ID).update(admin: true)`
