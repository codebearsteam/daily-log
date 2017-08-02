
### August 2nd ###  
Today was mainly about getting confused :) So here is a small recap of our process so far:
Our objective in this issue is to display the user's vote on a poll.  
We spent time learning about databases and creating test data in the local database in order to experiment.  
We then thought we would need to create a `show` action in the `poll_participation_controller` and then take care of the view, so we spent time learning about controller's actions and JavaScript basics, so we could follow the basic architecture of the model-view-controller.  
But! the `poll_participation_controller` probably is not related to solving this issue after all, because the view files are calling to poll-related methods from the model files. This is where our confusion started. Moreover, diaspora views don't use the standard HTML with erb, but HAML, Backbone.js and Handlebars.js, which we don't know at all.
We spent the coaching sessions today to research the diaspora code and trying to figure out where we need to add code. Our main suspects are:  
on the back-end side - `poll.rb`, `poll_presenter.rb`  
on the front-end side - `poll_view.js`, `poll_tpl.jst.hbs`  
Our tasks for tomorrow would be to keep researching the code and re-focus our learning efforts.

### August 1st ###

We started the day with two major tasks:
Configuring the broken computer so we could bring it back to the project. It worked! Finally we can both can have a computer each :)  
Creating more poll data on our local DB and practicing what we learned the day before. We made a list of the steps in order to create a poll in the DB. It goes like this:
1. create a `status_message` and pass to it `text` and `author` then save it
2. define a `poll` and pass to it `question`, the `status_message` we just created
3. create few `poll_answer`s and pass to each the `poll` we just defined and an `answer`
4. assign the `poll_answers` to `poll` and save poll
5. create `poll_participation` and pass to it an `author`, a `poll` and a `poll_answer`

After creating this data we need to add some code to the `poll_participation_controller`. In order to learn how to do that we watched the part on the `index` and `show` actions in our tutorial.  
Then we looked at the diaspora code, in the controller and the views. As always so far on diaspora things are not so straight forward and we need to do more digging and learning before we can write some actual code.   
In addition we had another git session with our git expert coach.


### July 31st ###

Today we first spent some hours watching the very helpful Lynda tutorial on ActiveRecords and ActiveRelation. It was a good supplement to the rails console session we had on Friday as it explained all the actions on the DB in detail. We learned a lot on creating, updating, deleting and finding records in the db through the rails console.
Then we went back to our second issue and created a Poll, a Status Message and Answers in the Rails Console. It helped a lot understanding better the code and database structure of the project, which is not so straight forward.
Tomorrow we will:
- create more users and polls
- play with the data
- solve some more git issues
- look at the poll_participations_controller.rb
