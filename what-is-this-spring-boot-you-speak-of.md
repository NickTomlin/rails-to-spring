# What is this spring boot you speak of?

At a previous job, I worked in a codebase that consisted of large Ruby on Rails monolith and several ROR "macroservices." The company had the admirable habit of hiring strong engineers who were not familiar with either Ruby or Rails. While this led to some fascinating "hybrid" approaches \(and the generally beneficial affect of having more than one way to look at a problem\), it also meant that engineers from certain backgrounds had a very rocky onboarding process. I found that engineers more familiar with Java would often struggle with the reliance on metaprogramming in Ruby applications \(e.g. how [`method_missing`](https://ruby-doc.org/core-2.5.0/BasicObject.html#method-i-method_missing) is use to achieve `find_by_<column>` in Active Record or Active Support's gleeful monkey patching of core classes\), the lack of strong typing, and the directory based wiring of a Rails application.

Whenever someone stumbled onto one of these road blocks I would hear something similar to the following phrase:

> "If we could just write this in Spring Boot it would be much better"

I was old and salty enough to know that this essentially translated to "I have used Java and Spring before, and I would prefer to use them now"; nonetheless, I was intrigued by the promise of something that would solve all my problems.

In my mind, Spring/Boot was "Rails without the rails": a more straightforward, less opinionated, service focused framework that would increase my velocity as an engineer. My mind was very very wrong.

## Setting expectations

I initially experienced a lot of frustration in my journey with Spring/Boot because I had the wrong idea of what that pairing of technologies was trying to accomplish. To counteract that, it's important to define what Spring and Spring Boot provide.

Spring boot provides a series of patterns built on the spring framework that covers the up-front cost of initializing and configuring a Spring application. It's a gateway to running an application on the Java ecosystem, not the opinionated, batteries included framework that Rails is. Spring _is_ opinionated in terms the way in that it enforces the registration of configuration and dependencies, but it is open to many different patterns at the application level. Unlike "the Rails way" which typically consolidates around one style of writing application code \(at least officially\), Spring seems to be very focused on providing a platform for a myriad of ways to accomplish things.

Additionally, Spring has it's own blend of magic. The extensive use of Java [annotations](https://en.wikipedia.org/wiki/Java_annotation) and autowiring of dependencies \(which can include _other_ auto wired dependencies\) make it difficult to understand how the different pieces of a spring boot application work together.

Initially I was a bit miffed that I'd been sold a dream that did not deliver on what it promised. Then, I realized that while there was a lot of up front cost, the flexibility and power of Spring provides a fantastic platform to build applications on.

