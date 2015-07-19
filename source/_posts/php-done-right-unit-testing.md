title: Unit Testing
subtitle: "Every single day a little bit better"
date: 2014-10-15 11:17:57
categories:
    - codecademy
---
### Unit Test is Important. Period.

* **Correctness**.
  With Unit testing, you can be certain, in a matter of seconds, that the code you wrote doesn't have bugs and behaves as expected.

* **Stability**.
  You can be sure that changes introduced in the future, by whatever developer, in whatever component of the entire system, aren't breaking existing functionality. You can advert a crisis by just having a failing test telling you something's wrong.

* **Design**.
  A Unit Test is a perfect proof of concept of how a specific component should behave, and how your code is supposed to be used. It shows how clear an API is, or how simple is to accomplish a certain task. It's the best documentation possible for any component.

### You should Unit Test APIs.

The general idea into Unit Testing, it's to configure a system, let it do it's work, and the check that the output is consistent with what we expected. This could be the desired output, or even an expected error if the input was incorrect. 

This viewing of the system to test as a black box that has an input and produces an output, could be extended from testing a single method, to an entire simulated request, depending on the level of integration you want.

### Test Example

Let´s get a fictional piece of code. The task is simple, we´re just representing a User model that uses a DB connection for fetching information. This User model implements a simple yet efective method for lazy loading the DB component, being at the same time open to accept modification.

{% gist 8454758 %}

What would we like to test in a scenario like this one? 

For starters, that the default implementation is being called when we don´t override it.

{% gist 8bcaeed88f9e652ff7bc %}

But this is just the beginning. Using [PHPUnit´s MockBuilder API](https://phpunit.de/manual/current/en/test-doubles.html) we can just create an exact representation of a `DBClass` and observe it´s `query` method, checking if it gets called properly. 

{% gist 8a4a89037f067002a905 %}

In the previous example, by using a Mock DBClass, and setting two expectations on its functionality (the fact that it gets called only once, and with "10" as a parameter) we can test the inner functionality of the `User` class by inspecting the behavior of its dependencies.



