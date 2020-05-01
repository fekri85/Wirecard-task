# Wirecard-task

This is the simplest playbook and jenkinsfile to install tomcat server
#Prerequisites
In Jenkins server, we should install Ansible, and Ansible Plugin and  create a Jenkins user

Jenkinsfile should work with a pipeline

#Playbook:
create a playbook to install and configure Tomcat with below tasks:

- updating repos on the server
- install minimum java 1.8.0 for tomcat 9
- downloading tomcat required tomcat version and unarchive to /usr/local/latest
- renaming tomcat home
- finally, running the tomcat with shell