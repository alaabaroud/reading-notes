# Read: 32 - Serverless and Amplify

So, What is Serverless?
Serverless is a cloud computing execution model that allows you to build and run applications and services without thinking about servers
serverless is one of the most used cloud services in upcoming years.

when you deploy the work, it will not be managed by you anymore and the responsibility is on the Cloud vendors. Serverless functions are accessed only as private APIs. To access these you must set up an API Gateway

Most projects have external dependencies, they work along with libraries that are not built into the language or framework itself. You'll  use libraries with functionality that includes cryptography, image processing, etc., these libraries can be pretty heavy. Without system-level access, you must package these dependencies into the application itself.

Functions as a Service (FaaS):
it is a category of cloud computing services that provides a platform allowing customers to develop, you can deploy a function or a piece of business logic. They start within milliseconds (~100ms for AWS Lambda) and process individual requests within a 300-second timeout imposed by most cloud vendors.

here are the sides that will be rendered and deployed:
- Client Application: The UI of your application is rendered client side which allows users to use a simple, static web server.
- Web Server: Amazon S3 provides a robust and simple web server. All of the static HTML, CSS and JS files for our application can be served from S3.
- Security Token Service (STS) — generates temporary AWS credentials (API key and secret key) for users of the application. These temporary credentials are used by the client application to invoke the AWS API (and thus invoke Lambda).
- User Authentication —  With Amazon Cognito, you can easily add user sign-up and sign-in to your mobile and web apps. It also has the options to authenticate users through social media like Facebook, Twitter or Amazon.
- Database — AWS DynamoDB provides a fully managed NoSQL database.
From business perspectiv
-------------------------------------

Overview
The GraphQL Transform provides a simple to use abstraction that helps you quickly create backends for your web and mobile applications on AWS. With the GraphQL Transform, you define your application's data model using the GraphQL Schema Definition Language (SDL) and the library handles converting your SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data model.
