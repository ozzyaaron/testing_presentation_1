# Outside-In Development

It's Less Boring Than Stamp Collecting!

!

# Why Test?

* Increased long term efficiency
* Increased deliverable quality
* Lower cost for staff induction
* Higher delivery rates to clients
* Increased ability to respond to customer demands
* Developer satisfaction - new features or old bugs?
* Developer satisfaction through constant small achievements. 
* Unshipped code is wasted time and money - reduce WIP and working *developer* capital
* Increase nose-in-air factor. 

!

# Outside In Testing

* About starting with integration testing
* Get inner ring tests passing (units & functional)
* To finally get the outer tests passing (integration)

!

# Outer Circle (Cucumber)

* Write your feature without training wheels just as you would say it
* ... and like your customer would say it
* Cut and paste example steps into step files
* Perform some step refactoring if needed
* Get to work

!

# Writing a Feature

*See features/activities/template_access.feature*

!

# Writing Step Definitions

*See features/step_definitions/activities/template_steps.rb*

*See features/step_definitions/general_steps.rb*

!

# Round the Outside, Round the Outside

* You should obviously hit issues.
* Quite likely the first is a missing route for new features.
* Then in the controller missing models and/or methods.
* Then in the model missing attributes or other models...

!

# Development by Wishful Thinking

* When writing your tests imagine the code is in it's best possible state. 
  * Nice method signatures
  * Form fields correctly labelled
  * Well named routes
  * etc
* Now write the code to make the tests pass
* You've now written well structured, easy to use code that other people will love you for 
* It's also, obviously, easy to test!

!

# Inner Circle (RSpec)

* Usually starts with controllers and routes
* Make the test for the necessary method call from your outer circle
* Write the calls in your test as you'd like to use them
* You're writing an API, don't be lazy!
* Doubles are great, they help you not be lazy and the outer circle makes sure the interfaces match

!

# Different Tools for Different Parts

* You're starting from the outside of the application and writing tests as you reach into the models
* Cucumber tests full stack but primarily drives views and controllers
* RSpec tests full stack too, but primarily better for controller edges cases and full model tests

!

# Where Should We Focus Right Now?

* I'm suggesting we focus primarily on Cucumber testing
* It's full stack so bang for buck is great. 
* It's easier to understand.
* Also do some model and controller tests as appropriate.

!

# Jenkins

* Continuous Integration server
* Lives at http:://jenkins.local:8080
* Pools github every 15 minutes for changes
* Build status is placed into team flow on flowdock
* Can do continuous deployment very easily
* Probably the best supported and highly used private build server for Ruby

!

# The Goal/s?

* \> 90% test coverage by year end
* Support and Sales writing *Cucumber style* documentation before feature work begins
* Warnings on checkins in model, controller, lib without spec or feature changes
* Automated staging deploys for green builds
* Push button production deployment :)

!

Questions
===
* Does you have them?
