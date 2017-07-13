### Issue /#6559 - Starting Phase ###

### July 13th ###

We had a-lot of progress in the past two days.

We realized what cases we have regarding the FROM header, and each one of them requires more work:

1. No sender present: when there in no sender, the from header is set to be: `AppConfig.mail.sender_address` -  the email address that is configured in the defaults.yml file. the default is a no-reply address, but the pod admin can configure this. The issue does not refer to this case. However, we saw that this case is not tested, so we wrote 2 tests, for 2 emails types with no direct sender in the notifier_spec.rb file, and asked on the issue if there are any more cases like that. You can take a look at our commit [here](https://github.com/codebearsteam/diaspora/pull/1/commits/2381602269b2fdcaf115cd760a74d9a6ac422419) if you would like.

2. Sender is present: just yesterday we understood completely this line of code: `headers[:from] = "\"Diaspora* (on behalf of #{@sender.name})\" <#{AppConfig.mail.sender_address}>" if @sender.present?`, that we changed in order to fix the issue. Apparently, the `.name` method returns one of the following options:

      a. First name AND/OR last name: In this case we are fine. Our code corrections answer to the requirements of the issue. we also changed the corresponding tests. You can see those changes [here](https://github.com/codebearsteam/diaspora/pull/1/commits/c5426e79328ed9bfc1e99c69afae5728065b30f5).

      b. Diaspora handler (for example podmin@podname.org): We actually don't want to have diaspora identifiers in the FROM header (as required at the issue), especially not something that looks like an email and confuses the recipient. Since we can't change the `.name` method to return just first name and/or last name but not a diaspora handler, we need to write a method in the base.rb file that does so. Since we also try to follow the TDD work flow, we already wrote a test for this case, and as expected it failed (\o/). The next step would be to write the method and see that the test passes (hopefully :)).  

That's it for today, it was a lot of fun :)

### July 12th ###

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
