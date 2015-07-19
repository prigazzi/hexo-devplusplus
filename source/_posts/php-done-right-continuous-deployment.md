title: Continuous Deployment
date: 2014-10-15 13:32:07
subtitle: "Our long-term objective"
categories: codecademy
---
In our constant effort to achieve Continuous Deployment, we´re working with several methodologies that allows us to be more agile in our development and deployment.

### Team Checks

After a significant ammount of work has been finished, its advisable that we show our progress to any team member and get feedback on the solution proposed. The solution may already been discussed with the team as a whole, but it's not a bad idea to check after again.

It the team member agrees that the proposed solution goes along with the one discussed with the team, then we´re ok to continue.

### Pull Requests

With our code ready and already commited to our personal fork, we're ready to create a **Pull Request** in Github. So far there´s a reduced list of persons that are allowed to accept Pull Requests and merge them to the master branch. Ask your team members and they´ll point you in the right direction.

{% youtube YTbRzhQju4c %}

### TeamCity and Deployment

Every single step of the way after you create a pull request, our TeamCity server will inspect you commit and run a series of processes and tests to ensure the new code does not affect the entire website. 

This type of inspection involves linting PHP code to **search for errors**, checking for the **adherence to current coding standards** and **running the unit tests** that will check that previous and new functionality keeps working properly.

After a Pull Request gets approved and merged into the master branch, this process runs again and only after this second check finishes successfully, we´re able to deploy the changes to our production servers.

While the checking is done automatically, the deploy process needs to be triggered manually for now. We keep on working to achieve the level of security that will eventually allow us to do this automatically also.


