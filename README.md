activiti-CustomUserManagement
=============================

Activiti - custom user management

Forum topics:
* Exchange IdentityService (or other services) https://community.alfresco.com/thread/215991-exchange-identityservice-or-other-services
* Use own User/Group-tables: https://community.alfresco.com/thread/215911-use-own-usergroup-tables
* How to Use own User Maangement instead of Activiti provided https://community.alfresco.com/thread/220239-how-to-use-own-user-maangement-instead-of-activiti-provided

This sample uses spring for configuration: src/main/resources/META-INF/spring/custom-activiti-beans.xml

Idea that 3 Activiti classes shoudl be changed:
* Explorer login should use custom implementatin./src/main/java/org/activiti/custom/explorer/ui/login/CustomDefaultLoginHandler.java 
* Custome User Manager factory that creates CustomUserEntityManager instead od UserEntityManager  ./src/main/java/org/activiti/custom/spring/CustomUserEntityManagerFactory.java 
* Custom User Manager services adapter ./src/main/java/org/activiti/custom/spring/CustomUserEntityManager.java
