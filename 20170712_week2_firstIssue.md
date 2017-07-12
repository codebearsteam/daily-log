### Issue /#6559 - Starting Phase ###

We have found the file app/mailers/notification_mailers/base.rb (line 42) to include the code that needs to be changed for this issue.
So far our approach is to

* change app/mailers/notification_mailers/base.rb (line 42) into: headers[:from] = "\"Diaspora* (on behalf of #{@sender.name})\" <#{AppConfig.mail.sender_address}>" if @sender.present?
* change app/mailers/notification_mailers/base.rb (line 37) into from: "\"Diaspora* \" <#{AppConfig.mail.sender_address.get}>" (We are not sure yet if this works)

#### Discussion on Diaspora ####
see [Issue /#6559](https://github.com/diaspora/diaspora/issues/6559)

#### Testing ####
* We have continued the tutorial on rspec: [Learn RSpec tutorial](https://www.tutorialspoint.com/rspec/rspec_introduction.htm)
* We have done some exercises on testing (writing simple example tests)
* Next step would be to write test for the actual issue we are working on

#### Open Questions / Discussion Point ####

1. There are different email cases:
a) sender present: in the examples above it says that the user gets emails from: "podmin@podname.org (diaspora*)" <no-reply@podname.org> or "Firstname Lastname (diaspora*)" <no-reply@podname.org>. Does line 42 apply for both cases? That means could sender.name be podmin@podname.org or Firstname Lastname?
b) no sender present: there should be only the no-reply@podname.org (AppConfig.mail.sender_address), which is true e.g. when I get a password reset link.
2. Also I sometimes get emails from "username@podname.org" not "Firstname Lastname" even though there is a sender present in this case. Where are the sender attributes defined? We found so far only the sender_address set to no-reply@podname.org, but couldn't figure out the other sender attributes. We guess that it must be stated somewhere that emails will be sent as Firstname Lastname or as username@podname.org
3. One small thing: When I get emails the name of the sender doesn't show as "Firstname Lastname" (diaspora*)but Firstname Lastname (diaspora*). I guess it is not so important but from the code I read that I should get emails the quotes.
