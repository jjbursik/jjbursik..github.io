---
layout: post
title:  "Jenkins Coded and Tested"
date:   2016-12-10
desc: "How to start up Jenkins locally on the Mac and test some Groovy DSL"
keywords: "blog,jenkins,groovy,dsl"
categories: [Code]
tags: [FirstBlog,HowToBlog,jekyll]
icon: icon-centos
---

Jenkins, while great, has its limitations if you don't build it correctly.  Several teams, products, etc. use Jenkins for a CI/CD tool and set up jobs through the Web Interface however then there is extra work to back up the jobs, save it somewhere, etc.  And, how do they ensure a job is set and not later changed over the course of time?  Well, it's simple... you use the Jenkins DSL.

Jenkins DSL is domain specific language and is basically a coded Jenkins job interface.  You still install Jenkins as usual however all jobs are saved into a code repository, pretty awesome huh?  My team introduced this to me and it's pretty slick.  However the problem for me, I like to test and develop locally which means I need a Jenkins instance running on the Mac that then reads from my Git Repository and builds all my necessary jobs.

Alright, here is how it's done, on a Mac:

Keep in mind, this worked for me however there were some struggles along the way.

1. Download Jenkins: https://jenkins.io/content/thank-you-downloading-os-x-installer/
2. Jenkins will download under a new username 'Jenkins' (this took me a little while to figure out)
3. Log into the new Jenkins user `sudo su Jenkins`
4. Generate an ssh key: `sudo ssh-keygen`
5. Save the ssh key into the GitHub repository
6. Jenkins should be running after the install at loclhost:8080, open and log in.
7. Download all the GitHub plugins you would like to use (for this purpose and at this time I used Git Plugin)
8. Set up a Global User Credential with the Id that you just created the SSH key for.
9. Create a job and point the SCM to you github account.
10. You should have some fun cloning now!

Now to the DSL.. to be continued...


Tips:

1. To stop Jenkins `sudo launchctl unload /Library/LaunchDaemons/org.jenkins-ci.plist`
2. To start Jenkins `sudo launchctl load /Library/LaunchDaemons/org.jenkins-ci.plist`
