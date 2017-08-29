### August 28th & 29th - next issue ###
This is gonna be our next issue: https://github.com/diaspora/diaspora/issues/1649
It´s about sending notifications to the contacts of a user (actually a Profile in Diaspora language).
As Neta is off this week, me, Rete has continued working on the issue this week.
After two coaching sessions today, this is the plan how to approach the issue from now on:

1. understand how the existing notifications work (important files and directories: `app/models/notification.rb`, `app/models/notifications`, `app/helpers/notifications_helper.rb`)
2. create new notification type which shows the birthday of a user to their contacts (here still without workers, just displaying the birthday in the Notifications)
3. get all of this working in the console
4. create worker that iterates over all profiles, checks if today is the birthday and then for each contact of the user calls the method in the newly created birthday notification type (see step 2) (important files and directories:`app/workers`, `config/schedule.yml`).
5. create NotificationMailer according to the other Notification types (important files and directories:`app/mailers/notification_mailers`, `app/workers/mail`)

From step 4 onwards it would be nice to use TDD as the steps are quite clear. For steps 1-3 it´s better to try stuff and play around until it works.
