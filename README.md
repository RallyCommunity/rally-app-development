rally-app-development
=====================

A tutorial for creating a development environment for Rally Apps

**Introduction**

The purpose of this guide is to help you create a productive environment for developing and testing Rally apps. It is aimed at those who might not have a lot of development experience or are not a full time member of a development team.  While following the steps of the instructions, refer to referenced screen shots for details.

**Principles**

- Comprehensive and collaborative source control in an environment that makes it easy to share and discover your work.
- Short feedback loops. Be able to test your app with real data immediately after making changes.
- Minimal or no requirement to install software locally.
- Consistent and standard approach.

**Components**

- Rally-App-Builder https://github.com/RallyApps/rally-app-builder
- Cloud9IDE https://c9.io/
- GitHub https://github.com/

**Getting Started**

You will need to (if you have not already done so) create accounts on github and cloud9. Both are free for basic use. 

**[1] GitHub**
--------------

- (1) Create a new repository (you will need to do so for each app that you create) on github. Be sure to check the box to create a readme.

![github repository](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-1.png)


**[2] Cloud 9**
---------------

- (1) Go to the Cloud 9 Dashboard (in your profile activate the github service).

![github cloud9](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_6_13_1_56_PM.png)

- (2) Find your just created github repository in the "Projects On Github" section of the project list. 

![github project](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_6_13_1_59_PM.png)

- (3) Select the project, and click "Clone To Edit", and select the project type "Custom".

![clone project](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_6_13_1_59_PM-1.png)

- (4) When the project is created, click "Start Editing" to open the project.  Note that it may take several seconds for the "Start Editing" button to show up.

**[3] Rally-App-Builder**
-------------------------

- (1) rally-app-builder is installed directly into your Cloud9 project workspace using node. From the "Terminal" window in your project type the following command.

 npm install -g rally-app-builder 

![node install rally-app-builder](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-7.png)

- (2) Once installed you initialize your Rally app with the following command

rally-app-builder init <enter your repository name here>

![init rally-app-builder](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-9.png)

- (3) This will create a skeleton project.

![init rally-app-builder](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-10.png)


**[4] Making changes to and testing your app**
----------------------------------------------

- (1) Edit App.js file, the sample below will add a button to your app.

items : [
        {
            xtype: 'rallybutton',
            text: 'Click me',
            handler: function() {
                Ext.Msg.alert('Button', 'You clicked me');
            }
        }
    ],

![code changes](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_3_13_2_52_PM.jpg)

- (2) Preview the app-debug.html file to see changes immediately. Note you can also copy the url from the preview pane into a new browser window if you would rather see your app fullscreen (also, once opened you only have to hit Refresh to immediately see changes to your app). Finally, log in to Rally in another tab to test apps which access Rally data.

![preview changes](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_3_13_2_52_PM-1.jpg)


- (3) 

![preview changes](https://raw.github.com/wrackzone/rally-app-development/master/img/Screenshot_7_3_13_2_53_PM-2.jpg)


**[5] Building the App and pushing to github**
----------------------------------------------

- (1) Use the following command to build the app. This will generate a new app.html file in the deploy directory. You can share a link to this file to distribute it and the contents of this file can be installed as a custom html app in Rally.

rally-app-builder build

![preview changes](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-11.png)

- (2) Add the code to github

git add . (note the dot after the word add)

![preview changes](https://raw.github.com/wrackzone/rally-app-development/master/img/git-add.jpg)

- (3) Commit to github

git commit . (note the dot after the word commit)

Enter your commit comments, once you have done that, hit "ctrl-X", then "Y", and hit enter, and you shoudl get a commit acknowledgment similar to the message below:

[master 63b18c7] this is a commit                                                                                                                              
 8 files changed, 135 insertions(+), 2 deletions(-)                                                                                                            
 create mode 100644 .gitignore                                                                                                                                 
 create mode 100644 App.js                                                                                                                                     
 create mode 100644 LICENSE                                                                                                                                    
 create mode 100644 app.css                                                                                                                                    
 create mode 100644 config.json                                                                                                                                
 create mode 100644 deploy/App-uncompressed.html                                                                                                               
 create mode 100644 deploy/App.html


![commit changes](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-12.png)

- (4) Push changes back to github repostiory

git push


![push changes](https://raw.github.com/wrackzone/rally-app-development/master/img/my-first-app-13.png)

- (5) You can now link to the app.html in the deploy directory.

![push changes](https://raw.github.com/wrackzone/rally-app-development/master/img/deploy-app-html.jpg)






