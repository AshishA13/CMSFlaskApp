# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

::Analysis::
Azure App Service: 
1. App service is a platform as a service and take away most of the customer responsibility and give it a cloud provider. Developer needs to take care of their application and data only. All the other infra related responsibilities 
   stay with provider.
2. Is a managed platform where one needs to focus on building the app only. Azure would take care of Deployment and management. 
2. This helps instant deployment and vertical scaling as well as redeployment
3. This is easy to manage but lacks support for legacy apps.
4. It limits on the exponential growth of the project or have plan to expand the user base. But a great choice for some small application.
5. This does not allow pay as you go option, so once you get the App service you need to pay for it even though you are not using it (like the apps you deployed, there are limited user and use is also limited)

Virtual Machine:
1. This is an example of IaaS, Infrastructure as a service. Where Infrastructure like Networks, storage, servers and virualization service is provided by the service provider. User or organization still needs to take care of their  
   applications, data, runtime, middleware and OS.
2. With virtual machine you will have full control over application management as well as deployment. Having said that, 
3. This is a best option for projects which demands change on technology stack front or vendor, VM would handle this with ease.
4. Added services come with the added work. Developer may still need to manually configure the application server or framworks, take cares of OS updates, configuring security
4. Once needs to put additional efforts to manage all the activities but provide great support to leagacy apps.
5. Application expansion won't be an issue in future, highly scalable.
6. This is expensive compare to App service but have option pay as you go, so if you are not using it you won't bill for the service.


::Chossing a best solution for the this application::
CMS flask application is a small app which has few fields, SQL db and blob for storing data. Looking at the scope and maintainability this is a great candidate for app service. This application needs to up all the time and should have interupted access to user. Considering the usability, time needs to spend on maintaining, app service would be a great choice for this application. That way, it would be cost effective and don't need to worry about managing variants of services needed to run it.

::Justify your choice::

CMS Application mainly using flask framwork and python as development language. Also, the field on the app are limited which can be easily manage with the App service. It store the data in SQL database and images on blob. 

Looking at the CMS Flask application criticality, it should be good to focus on making the application most user friendly and use web service for the deoplyment only. 



### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

In future, if the scope of the application expands (Technological expansion, more users, more functionalities, criticality) then it would be a wise choice to go into Virtual Machine mode. This would definitely add cost but will serve the users demand and don't meed to worry about price if not in use.  
