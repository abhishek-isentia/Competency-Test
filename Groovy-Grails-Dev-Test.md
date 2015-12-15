# Coding challenge
This page consists a set of coding challenges for Groovy/Grails developer role at iSentia.

# Purpose
Aim of this test is three fold,

- evaluate your coding abilities 
- judge your technical experince
- understand how you design a solution

# How you will be judged
You will be scored on,

- coding standard, comments and style
- unit testing strategy
- overall solution design
- appropriate use of source control

# Intructions

- Please use Groovy, Grails, MongoDB, and RabbitMQ
- Candidate should put their test results on a public code repository hosted on Github
- Once test is completed please share the Github repository URL to hiring team so they can review your work

# Challenge - Flickr feed viewer and search

- Write a simple web application that reads data from Twitter public search APIs and stores them into MongoDB. 
- Please check the following API documentation from the following URL:

- [Twitter Search API]( https://dev.twitter.com/rest/public/search)
- [Twitter Streaming APIs](https://dev.twitter.com/streaming/overview)


## Details

- Write a web application built using Groovy, Grails, MongoDB, and RabbitMQ
- On page load the applications should render a search box.  
- The user should be able to enter a keyword or hashtag in a search box and click on a search button
- The app should return the relevant Tweets without page load
- Use APIs and Ajax to load results on search page
- Use any other third party library of your choice if needed 

You can use the [Twitter Bootstrap](http://getbootstrap.com/) to make your application look good and responsive.

Bonus point, if you deploy the app as a public site using Amazon EC2 instance.
