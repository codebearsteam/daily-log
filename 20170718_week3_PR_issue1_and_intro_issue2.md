## Issue #4888  ##

### July 20th - work on PR of first issue ###

Today started with a very productive retrospective. We are really happy about the outcome and we feel like we are on the right track :) Thanks to all our coaches for all the support in the past weeks!
Then we had a coaching session about Continuous Integration. We learned about the concept in general and ran the checks (pronto) that we actually should have run before our first PR :)
After that we went back to the comments we got on our PR, ran pronto again and fixed the small things that it was warning us about.
We made the decision on having the pod_name instead of "Diaspora*" in the header as it was suggested in our PR.
Then we ran all the tests and checks (rspec, jasmine, cucumber, pronto) and got all of them green except for cucumber. As the failures were not on parts of the code that we touched in our work, we decided to commit and push. We will ask on the PR about the failing cucumber test.
In this process we also learned a lot about discussing with the community and running tests and checks before opening a PR.
Now we're waiting for more feedback from the project.

Topics covered:
* Continuous Integration
* testing
* refactoring



### July 19th - work on PR of first issue ###

Today we mostly dealt with fixing the comments on our PR.
We did a list of all the corrections needed to be fixed or discussed.
On our way to fix the code, we had some problems with git (couldn't pull the code to one computer) and with ruby versions discrepancies. We got a lot of help from our coach working on this. Afterwards we jumped right into fixing and refactoring the code, making the relevant test fail and then making it green, very satisfying very satisfying. We corrected almost everything, the rest we will do tomorrow. You can see the entire comments and discussions here.
In between we had a session with SC IT team in order to get external company emails and organized our 1st retrospective meeting :).

### July 18th ###

We started to work today on [this issue](https://github.com/diaspora/diaspora/issues/4888). It involves a list of issues regarding poll features. We read the issue and the entire discussion alongside testing polls creation on our own diaspora profiles, and came up with a list of 9(!) improvements. In our coaching session we divided the list to two categories:

Visual issues:
1. radio buttons alignment.
2. delete icons alignment.
3. enable label voting (in the discussion on the issue it is said that this is solved but it actually doesn't work in the poll we created).

Missing behaviors:
1. enable to shut down poll/time limit voting.
2. mark the option the user voted for.
3. enable mobile voting.
4. enable re-sharing poll (like any other status).
5. enable to edit privacy settings after poll was created.
6. enable to publish the poll without wring a status (there is already a field for the poll question, so adding a status on top of that seems sometimes unnecessary).     

We don't know if we actually will tackle all those issues, and we still need to choose some and prioritize.

In any case, after a quick look at the code we have realized we need to learn about Active Records and ORM, so we are looking at some videos and tutorials:
* [Rails guide for Active Records](http://guides.rubyonrails.org/active_record_basics.html)
* [envato tuts+](https://code.tutsplus.com/tutorials/active-record-the-rails-database-bridge--net-30489)
* [Rails cast](https://www.youtube.com/watch?v=96RIkuwA1h0)
* [LaunchCode introduction to ORM](https://www.youtube.com/watch?v=dHQ-I7kr_SY)
* [Linda Ruby on Rails course](https://www.lynda.com/Ruby-Rails-tutorials/Understanding-ActiveRecord-ActiveRelation/139989/159093-4.html)
