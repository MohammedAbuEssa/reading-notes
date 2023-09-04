# API Integration

[Review API Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/)

1. Explain the different between a query string parameter and a path parameter.

Query string parameters are used for non-hierarchical data and are appended to the URL with a question mark, while path parameters are used for structural or hierarchical data and are part of the URL's path segment.

2. What would our API URL with a path id parameter be given the following information:

Domain: `http://our-site.com`  
`v3`  
model name: `stuff`  
id: `things`

1t should be like this : `http://our-site.com/v3/stuff/things`

3. We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend.

Think of the dynamic API's interface like a user-friendly control panel. It displays buttons and forms, similar to a vending machine's options. You click the buttons or fill in the forms to make requests, like ordering a snack. The API then processes your requests and sends back responses, just like the vending machine delivers your snack. It's a simple way for people, even without technical knowledge, to interact with and get things done through the API.

[Review Auth Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/)

1. Describe how you would use middleware to implement basic and bearer auth.

`Basic Auth` : It's intercepting the incomnig request then We decoded the data using base-64 then check if the is exist in the database if yes we will allow the users to get what they need within thier premission and give them token.

`Bearer Auth` : It's intercepting the incomnig request and check if the token is valid we will allow the users to get what they need within thier premission.

2. Describe the handshake necessary to implement OAuth.

This handshake process ensures that the user's data remains secure and that the client application can access only the resources the user has explicitly authorized. OAuth is widely used for enabling secure third-party application integration and authorization across various online services and platforms.

3. Describe how Role Based Access Control works to a non-technical friend.

Restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.
