## Sinatra versus Rails Exploration

### Setup:

First, clone down the Rails project:

```terminal
git clone https://github.com/turingschool/job-tracker.git rails_project
```

And then clone down the Sinatra project:

```terminal
git clone https://github.com/turingschool/bike-share.git sinatra_project
```
Now cd into each project, run `bundle` on each project, and you're ready to go. We will only be looking at the code base and not interacting with the app. If you wanted to run the server and interact with the app, you would need to create your database, migrate your migrations, etc.

### Exercise:

1. Take a look at this stripped down Sinatra app and this stripped down Rails app. How are they different and how are they similar? Identify 5 differences, and for each one describe 1-2 implications. What effect does that difference have for each framework? If you don't know exactly, draw on your knowledge and experience and make some educated guesses/inferences. Also, practice your research skills to look into the differences.

In the rails app there is an assets folder, containing 3 more folders inside of it, that looks to be setup for more advanced usage of Java Script and HTML.  It is still holding a MVC and the views folder is still present.  The Sinatra app just uses our standard MVC format.

The rails app in general seems to have a lot more structure setup with "file"helpers.  This makes me believe it is set up to run processes more smoothly.  These helperfiles seem to be there because of the gemfiles we are using in rails app.

The gem files are almost completely different.  Sinatra based gem files and ones that help rails app work better.

The rake files are different too.  Sinatra uses ActiveRecord to help with its rake functions.  Rails app is doing it, on it's own.

Our rails app uses a yaml database, while sinatra is building a database through standard ruby code.  Yaml I just read is a built in ruby library that is better to deal with large databases or content.  This makes sense since it seems our rails app will be doing a heavier work load than our sinatra app.    (Also in my reading, the other database that ruby has built in is Pstore.  I'm curious why we haven't used that in Turing at all)


1. Consulting blogs and commentary you find online, identify 3 similarities between Rails and Sinatra.
    They both have some overlapping scopes in terms of web application.

1. Consulting blogs and commentary you find online, identify 3 things that distinguish Rails, advantages.
    Sinatra is great for dealing with micro-style while rails is better if you go beyond micro.
    Sinatra would be your code, allowing you to choose the degree of control you have over your app; whereas Rails is built on frameworks and gems that don't offer you the amount of control you have, but for the benefit of having something run with more ease.
    With working in strict time frames you might want to consider using rails,  as sinatra while it is your own code, it takes longer possibly to implement logic or deal with problems.  Rails avoids these issues.
1. In your Rails project, what does the `routes.rb` file inside of the `/config` directory do? What does this correlate to in our Sinatra app?

1. We teach Sinatra by adding some structures that Sinatra doesn’t need, but help you make the transition between Sinatra and Rails. What does a stripped down implementation of Sinatra look like, and what are the pieces we’ve added for educational purposes?
      I believe gemfiles.  The sinatra looks bare to me, in my readings, I found that people liken the ruby practice of small broken down pieces to sinatra.  In a sense that if you have small applications you should use sinatra, then if you find that you need something that sinatra is missing, you most likely can get a gem to take care of it for you.  Or if sinatra is missing something that is a little more meta like a web hoster, you could then outsource those issues with little effort and synchronization. 
