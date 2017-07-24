### July 21st ###

Today we worked on further comments on our PR, got git messed up again and managed to solve that finally. The build returned green!!!
Because the we couldn't figure out the git flow yet, we dedicated our coaching session to git basic. We spent 2 very useful hours on this topic and gonna pick it up from the same point next week. As diaspora flow refers only to one person working on a specific branch, we need to figure out how the flow would be with 2 people working on the same branch.
Other then that, one of our laptop died and didn't seem to wanna become alive again. Task for the weekend: fixing the laptop with hopefully no data loss...


### July 20th - work on PR of first issue ###

Today started with a very productive retrospective. We are really happy about the outcome and we feel like we are on the right track :) Thanks to all our coaches for all the support in the past weeks! You can find the action items from it [here](https://github.com/codebearsteam/daily-log/blob/master/assets/1st%20_retro_action_items.JPG)
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

We started to work today on [this issue](https://github.com/diaspora/diaspora/issues/4888). It involves a list of issues regarding poll features. We read the issue and the entire discussion alongside testing polls creation on our own diaspora profiles, and came up with a list of 9(!) improvements. We don't know if we actually will tackle all those issues, and we still need to choose some and prioritize. At this point we left this issue and handled the rest of the week with the first issue's PR.

As we came back to this only the following week, you can see what we have done with this issue [here](https://github.com/codebearsteam/daily-log/blob/master/20170724_week4_issue2.md)  
