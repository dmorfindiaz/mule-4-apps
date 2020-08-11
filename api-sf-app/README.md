# api-sf-app

api-sf-app that can be used to consume Account records from 2 different Salesforce instances using different endpoints. 
It contains an API specification with the below methods:

• Get all accounts

• Get single account

• Post single account

• Put single account

• Delete single account


Get methods generate CSV files but they only can be seen when the application runs on local or when there is another place like a server to drop the files.
“Get all accounts” and “Get single account” create separate CSV files with the next format type
{app.home}/files/{type_+time_in_nanoseconds_.csv}
Example:

• Get all accounts: /opt/mule/mule-4.3.0/apps/exercise-sf-app/files/multiple_accounts_980000000.csv

• Get all accounts: /opt/mule/mule-4.3.0/apps/exercise-sf-app/files/single_account_648000000.csv

To consume the endpoints, the developer needs to provide client_id and client_secret.
client_id & client_secret can contain random names when the application is on local or when the application is deployed on cloudhub but the client Id enforcement policy is not enabled on API manager.

If client Id enforcement policy is enabled on API manager, user needs to use below credentials

• client_id: c6b20f34a76e400c96bfdfefde3a3319

• client_secret : D491f3F368A74592A15a29bEBa8500E5

The correct endpoints for each method will be provided in the Postman Collection (Attached to the email)

To be able to work with API manager, (tool that gives us the functionality of our client Id enforcement policy), we need to make sure that the bellow properties are added to our project

anypoint.platform.client_id=b5aad327b27541558c4769acbb226c0a

anypoint.platform.client_secret=B6C484D61d0642a4804B55C02Ee107Db

api.id=16286403

Notes:
api.id (for autodiscovery)
API Autodiscovery is a mechanism that manages an API from API Manager by pairing the deployed application to an API created on the platform

Mulesoft has been configured to read the dev properties by default. This was done using the Global property configuration on anypoint studio. 


The below endpoints can be consumed by using the postman collection attached to the email or to the drive folder.

•	Get single account

•	Post single account

•	Put single account

•	Delete single account

