The sample code in this folder demonstrates how to utilize the PI Web API in Angular. You must have already [configured your Angular development environment](https://angular.io/guide/quickstart) in order to run this sample application.  


Getting Started
------------

To run the sample code:
- Clone the GitHub repository
- Open the Angular\AngularPIWebAPISample folder with your IDE
- Install the required modules by running the following command in the terminal:  ```npm ci```
- Run the application using the following command in the terminal:  ```ng serve```
- By default, you can open the Angular app by using the following URL in a browser:  ```localhost:4200```

Getting Started with Tests
------------

To run the sample tests:
- Open the test file:  ```Angular\AngularPIWebAPISample\src\app\services\piwebapi.service.spec.ts```
- Search for the text __const piWebAPIUrl__, add your PI Web API Url.  For example:  

```typescript 
const piWebAPIUrl = 'https://mydomain.com/piwebapi';
```

- Search for the text __const assetServer__, add your Asset Server Name.  For example:  

```typescript 
const assetServer = 'AssetServerName';
```

- Search for the text __const piServer__, add your PI Server Name.  For example:  

```typescript
const piWebAPIUrl = 'PIServerName';
```

- Search for the text __const userName__, add your PI Web API user name.  For example:  

```typescript
const userName = 'MyUserName';
```

- Search for the text __const userPassword__, add your PI Web API user password.  For example:  
```typescript
const userPassword = 'MyUserPassword';
```

- Search for the text __const authType__, add your PI Web API authentication method (Basic or Kerberos).  For example: 

```typescript
const authType = 'Basic';
```

- In the terminal, use the following command to run the tests:  ```ng test```

System Configuration
----------------------------

In order to run this sample, you must configure PI Web API with the proper security to:
- Create an AF database
- Create AF categories
- Create AF templates
- Create AF elements with attributes
- Create PI Points associated with element attributes
- Write and read element attributes
- Delete all the above AF/PI Data Archive objects  


In addition, PI Web API must be configured to allow CORS as follows:  

|Attribute|Value 
------|------------
CorsExposedHeaders|Allow,Content-Encoding,Content-Length,Date,Location  
CorsHeaders|*  
CorsMethods|*  
CorsOrigins|*  
CorsSupportsCredentials|True  
DisableWrites|False  


Functionality
--------------

This sample shows basic functionality of the PI Web API, not every feature. The sample is meant to show a basic sample application that uses the PI Web API to read and write data to a PI Data Archive and AF. Tests are also included to verify that the code is functioning as expected.

The functionality included with this sample includes(recommended order of execution):
- Create an AF database
- Create a category
- Create an element template
- Create an element and associate the element's attributes with PI tags where appropriate
- Write a single value to the attribute
- Write a 100 values to an attribute
- Perform a Batch (6 steps in 1 call) operation which includes:  
  - Get the sample tag  
  - Read the sample tag's snapshot value  
  - Read the sample tag's last 10 recorded values  
  - Write a value to the sample tag  
  - Write 3 values to the sample tag  
  - Read the last 10 recorded values from the sample tag only returning the value and timestamp
- Return all the values over the last 2 days
- Return timestamp and values over the last 2 days  
- Delete the element
- Delete the element template
- Delete the sample database

[![Build Status](https://osisoft.visualstudio.com/NOC/_apis/build/status/PI%20Web%20API%20(Angular)?branchName=dev)](https://osisoft.visualstudio.com/NOC/_build/latest?definitionId=4612&branchName=dev)  

For the main PI Web API page [ReadMe](../../)  
For the main landing page on master [ReadMe](https://github.com/osisoft/OSI-Samples)
