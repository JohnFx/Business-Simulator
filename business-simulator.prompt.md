Please create a web application as described below



Overview: An educational application for students that simulates running a business to teach students about running a business.



There will be three classes of users: Students, Teachers, and Administrators



Functionality: 

&#x20;- Students can create an account in the application that they will use to login to the application.

&#x20;- Once logged in students can create one or more business profiles and define basic information about the business such as the type of business, add a logo, and a textual description of the business.

&#x20;- Students can invite other student accounts to each of the business profiles so they can work collaboratively managing the business

&#x20;- Teachers will be able to see all student accounts and the businesses for each.

&#x20;- Students will be able to make core business decisions and update them each day such as budgets for marketing, sales, R\&D, and prices

&#x20;- Teachers or Administrators can trigger an iteration of the simulation that will consider inputs for each business, inputs from other businesses in the market and some randomized market factors to determine outputs for that round of the simulation

&#x20;- After each round each business will be updated with basic financial statements and a summary of business performance for that round and a historical analysis of the business to date.

&#x20;

Authentication:

\- simple password authentication 

\- password reset functionality using the email on the users profile

\- Administrators should be able to view, edit and delete all user accounts





It should use the following tech stack

\---------------------------------------

Architecture: AWS Serverless

Database: AWS RDS MySQL

Backend: AWS Lambda built in C#

Frontend: HTML5, jQuery UI, Vanilla JavaScript

Authentication: AWS Cognito

Containerization: None

Availability: Single-AZ for all components





A goal for this project is to keep the operating costs as low as possible.













