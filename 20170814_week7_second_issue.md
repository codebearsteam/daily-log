### August 17th ###

We started the day with another nice retrospect.
The rest of the day we spent mainly on getting our code ready for the pull request.
We cleaned the code after cleaning the code according to the checks results , we fetched changes from the project's remote, committed our changes and rebased our branch, alongside we fixed some conflicts and squashed irrelevant commits- following our git work-flow before a PR.
But! after we fetched the changes from the project's remote we started having problems.
We had to install gems that were missing, and lots of tests failed now... we fixed the tests we knew how to fix, but most of the failures were related to migrations. With the help of our coach we realized it's probably it is related to problems on our local machines and we ran g rake db:migrate. It didn't work so we couldn't figure it out completely just yet. That will have to wait for next week.
On the other hand, we decided that we can still open the PR and work on all the fixes together, so we did :).

### August 16th ###

Today we made some big progress on our issue and we will open a PR tomorrow. We had some correspondence with the diaspora community on the Jasmine tests, which was very helpful. Then we were able to write the front-end tests on the users vote. Then we ran the pronto checks which we will take care of tomorrow.


### August 15th ###

Today we did come recap on CSS and got an introduction to SCSS from one of our coaches. This was very helpful to understand the CSS in our code. We then went over to editing the css in our code so the progress bar would change color instead of the text. The only thing left on this end, is to remove one line of code regarding different color themes that the user can choose in their profile.
In the afternoon we started looking at the Jasmine tests and realized that we had many many failures because we didn´t use an if-statement when extending our defaultPresenter. After solving this we have 4 Jasmine tests failing which we left for tomorrow. We will also start adding our own Jasmine tests for the Javascript we wrote.


### August 14th ###

We focused on writing rspecs for our ruby code for this issue. We had to refresh our memory a bit but at the end we wrote two tests: `poll_spec.rb:27` and `post_presenter_spec.rb:90`. The most complicated thing was to create all the relevant variables for the tests. The coaching session was very helpful for that.
We also learned a-lot about how to use a debugger in order figure out what is not working. We also learned what possible problems that could rise from using the `id` attribute and how to avoid using it as much as possible.  
Even though it was a bit slow, at the end of the day we have two good tests on the back-end side. The challenge for this week would be to write front-end tests, which we never did before.
