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

* Declarative vs Imperative scenarios
* Sharing variables within scenarios for nicer steps

!

# Writing Step Definitions

*See features/step_definitions/activities/template_steps.rb*

*See features/step_definitions/general_steps.rb*

* Demo World()
* Reusing steps

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

* RSpec is a BDD tool that is used for unit testing
* Test the outcome/behaviour rather than what it's doing
* Usually starts with controllers and routes and moves in to models/libs
* Make the test for the necessary method call from your outer circle
* Write the calls in your test as you'd like to use them
* You're writing an API, don't be lazy!
* Doubles are great, they help you not be lazy and the outer circle makes sure the interfaces match

!

# Using RSpec

* Context/Describe are the same
* it "", it { }, its(:sym) { } sometimes some are better than others
* it is implied by the subject/describe
* let() & let!()
* subject {}
* before {}, before do end, before(:each), before(:all), after...
* Test & Context/Describe strings concatenate for docs

!

# Different Tools for Different Parts

* You're starting from the outside of the application and writing tests as you reach into the models
* Cucumber tests full stack
  * Primarily drives views and controllers
  * It's generally about best-case scenarios
* RSpec can do full stack too
  * Primarily better for controller edges cases and full model tests
  * Sweep up whats leftover from the best-case tests (Cukes)

!

# Where Should We Focus Right Now?

* I'm suggesting we focus primarily on Cucumber testing
* It's full stack so bang for buck is great. 
* It's easier to understand.
* Also do some model and controller tests as appropriate - using RSpec.
* Big IMPACT with little effort!
* Money creation paths - user signup, activities, planning, supplier features
* Money retention paths - reporting, messaging, weather, etc

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

* Have fun. Testing should make you feel like you're doing more, more confidently.
* \> 90% test coverage by year end
* Support and Sales writing *Cucumber style* documentation before feature work begins
* Warnings on checkins in model, controller, lib without spec or feature changes (by 06/2012)
* Automated staging deploys for green builds by year end (coverage dependent)
* Push button production deployment - the future! :)

!

# Coming Soon ...

* How to use Factories
* How to use FactoryGirl
* Best practices for acceptance tests (Cukes)
* Best practices for functional tests (RSpec)

!

Questions
===
* Does you have them?
