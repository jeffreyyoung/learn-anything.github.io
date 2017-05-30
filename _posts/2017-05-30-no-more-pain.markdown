---
layout: post
title: "No more deployment pain :whale2:"
date: 2017-05-15 15:18:00
categories: Automation
author: Angelo
---

In the last few days we published some big updates, and unfortunately that meant
some hours of downtime. The problems were that we didn't take into account the
differences between our environments and the server, and we didn't automate the deployment
system. However, today that has changed, and there shall be no more pain.

#### Differences between environments
When we first tried to update the website, we simply pulled the changes we made and run `npm install && npm start`. This way we'd install the missing dependencies, build the project and start serving the website. Unfortunately we didn't realize until it was too late that the server has only 512MB of RAM, and that is not enough to build the dependency tree for then fetching all needed packages.

To solve this problem we installed the dependencies from another machine and then uploaded them on the server. However `node-sass` is a native module and in our case, the code was being compiled for Mac OS, while the server is running Ubuntu.

Lastly we decided to build the project locally and upload the compiled code to the server. Which finally worked!

#### Manual deployment
Having deployed the website really few times before, we didn't spend too much time on automating this process. We just ssh'd into the server, pulled the new version and build it. Each time. After the new big update though we plan to push updates live much more often, so this is definitely an issue that had to be addressed.

#### The solution
The solution was automating the process and getting rid of the environment differences. Here's where Docker came to help. Docker is a tool that makes it easier to deploy and run applications by using containers. Containers allow you to package an app with all its dependencies. You also don't need to worry about what OS you're running the container on, as Docker offers you an additional layer of abstraction.

<img alt="img" src="https://raw.githubusercontent.com/learn-anything/img/master/docker-workflow.png">

The new workflow we set up allows us to work completely on improving the search engine. Whenever we want to make a new release, we just push to the master branch on GitHub, Docker will automatically build an image, and the server will fetch it to create a new container.

#### TL;DR
We fully automated our deployment system. Now we just push to the master branch to put changes in production. All this is possible thanks to Docker magic :whale2:.
