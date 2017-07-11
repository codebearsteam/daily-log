### July 11th- The past week summery ###

We started approaching the project with Diaspora's [contribution guide](https://wiki.diasporafoundation.org/Getting_started_with_contributing).   
Especially we focused on getting familiar with Diaspora's [git work-flow](https://wiki.diasporafoundation.org/Git_workflow) and [testing work-flow](https://wiki.diasporafoundation.org/Testing_workflow).

After this introduction we are now working on few subjects in order to be more ready:

* Testing: As we started the project with zero knowledge about testing we dived into tutorials, videos and exercises. We didn't yest read or watched all of them but we are working on it. This is the stuff we have so far:
[Learn RSpec tutorial](https://www.tutorialspoint.com/rspec/rspec_introduction.htm),
[Everyday Rails blog post about testing](https://everydayrails.com/2012/03/19/testing-series-rspec-models-factory-girl.html),
[TDD exercises](https://sites.google.com/site/tddproblems/all-problems-1/text-editor-end-of-line-trimming),
[Code School video](https://www.youtube.com/watch?v=Dj19O9kLK6w),
[Rail-cast video](https://www.youtube.com/watch?v=AQ-Vf157Ju8),
[Sandi Metz talk](https://www.youtube.com/watch?v=URSWYvyc42M).

* Github: We are figuring out some git basics with [this tutorial](http://rogerdudler.github.io/git-guide/).

* Mails: The subjects of emails in general, and in rails in particular, is also brand new for us. We started reading Rails [Action Mailer Guide](http://guides.rubyonrails.org/action_mailer_basics.html) and the related [documentation](http://api.rubyonrails.org/) in order to get familiar with the subject, [Rails-cast video](https://www.youtube.com/watch?v=OI-m0wbmf8A) was also helpful.

[Issue #6559](https://github.com/diaspora/diaspora/issues/6559): While learning, we started to look at our first issue. We located the code that need to be fixed for the issue in app\mailers\notification_mailers\base.rb, lines 35-40. We located the related test in spec\mailers\notifier_spec.rb. We realized there is a bit of a gap between the issue description and the code. We will ask about that on the Diaspora IRC channel.
