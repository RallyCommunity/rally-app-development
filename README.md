rally-app-development
=====================

A tutorial for creating a development environment for Rally Apps

Introduction

The purpose of this guide is to help you create a productive environment for developing and testing Rally apps. It is aimed at those who might not have a lot of development experience or are not a full time member of a development team.

Principles

- Comprehensive and collaborative source control in an environment that makes it easy to share and discovery your work.
- Short feedback loops. Be able to test your app with real data immediately after making changes.
- Minimal or no requirement to install software locally.
- Consistent and standard approach.

Components

- Rally-App-Builder https://github.com/RallyApps/rally-app-builder
- Cloud9IDE https://c9.io/
- GitHub https://github.com/

Getting Started

You will need to (if you have not already done so) create accounts on github and cloud9. Both are free for basic use. 

GitHub

- Create a new repository (you will need to do so for each app that you create) on github. Be sure to check the box to create a readme.

![github repository](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-1.png)


Cloud 9

- Go to the Cloud 9 Dashboard (in your profile activate the github service).

![github cloud9](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_6_13_1_56_PM.png)

- Find your just created github repository in the "Projects On Github" section of the project list. 

![github project](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_6_13_1_59_PM.png)

- Select the project, and click "Clone To Edit"

![clone project](https://github.com/wrackzone/rally-app-development/blob/master/img/Screenshot_7_6_13_1_59_PM-1.png)

- When the project is created, click "Begin Editing" to open the project.

Rally-App-Builder

- rally-app-builder is installed directly into your Cloud9 project workspace using node. From the "Terminal" window in your project type the following command.

![node install rally-app-builder](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-7.png)

- Once installed you initialize your Rally app with the following command 

![init rally-app-builder](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-9.png)

- This will create a skeleton project.

![init rally-app-builder](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-10.png)










