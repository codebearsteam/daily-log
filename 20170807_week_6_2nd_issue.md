
### August 10th ###
We continued our struggle with the issue, here is the summery of our it:
We’re not sure what is the best way to display the answer the user voted for in the template. We get all the data in the Poll JS model, but we don’t really know what would be the best way to go from there to displaying it in the template.
Other then struggling we:
* Kept watching the front end related tutorials ans digging in the code with our coaches. We are still at the same point but we understand a bit better what is going on.
* Kept refactoring the back-end methods and now they look really nice.
* Had a very nice meeting with another team that worked on diaspora over SoC 3 years ago. We got some good tips and a lot of encouragement. It was very necessary after this long week of struggling :)

### August 9th ###
We spent the day in two main tasks:
1. Continuing tutorials on JavaScript, Backbone and Handlebars. It's a lot to take in so it takes us a lot of time.
2. Getting human help on the front end side of our issue:
* we had a remote coaching session which helped us understand a bit more the poll_view.js file.
* we turned for help to the SoundCloud developers channel to check if there is someone that actually knows Backbone and Handlebars, and set a coaching session specific to this topic on Friday.
* we had a helpful session about JavaScript applications in general and their own MVC architecture.

### August 8th ###
Today we mainly continued working on our database query, created a JOIN and made it work. Then we realized it needs more refactoring, so we did that as well.
We also checked with the diaspora community about the way our users vote should be displayed in the browser. From the feedback we got, it looks like we need to dive deeper into Handlebars and Backbone and also we might not need the JOIN after all. We also started looking at the Handlebars templates which we will continue tomorrow.

### August 7th ###

Today we started the day with recapturing what we did on Friday. We decided that we need to understand more of Backbone.js so we started watching tutorials on this JavaScript library.
In the afternoon we started looking at our solution from Friday especially with respect to the database query. We got the hint that we should make one query instead of two, so we would have to do a JOIN. So we first looked at the psql console to learn about JOINS and then went to the Rails console to see how JOINS work in Rails. Tomorrow we will go back to our code and see how we can change the query using a JOIN.
