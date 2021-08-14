# Chapter 15
In this chapter, We deployed our application using heroku to the internet. We used mongo Atlas to put our local database in cloud platform for serving the purpose of application deployment.


Link to my application:
https://tracker-ui-janvidankhara.herokuapp.com
### Screen shot
![](/readme_images/CH15.png)

### Problems faced while working on chapter 15
- Got stuck on how to create a MongoDB Atlas url.
- I was getting error saying password must be string encoded. Later on, I figured out that if password has special characters in password must be encoded.
- Got error after deploying heroku app saying cookie-parser not found. After adding cookie-parser it was showing the same. After committing and clearing the cache this problem got solved.

# Chapter 14
This chapter works on google sign-in allowing only authorized user(SignedIn user) to perform specific tasks such as create issue, delete and close issue. It uses Google Authentication API to allow users to login using client_ID created from Google credentials. At last we changed the domain to ui.promernstack.com:8000 by adding a line in etc/hosts and setting the origin to ui.promernstack.com:8000.

### Screen shot
![](/readme_images/CH14.png)

### Problems faced while working on chapter 14
- While adding google sign-in was facing an error Missing enviroment variable GOOGLE_CLIENT_ID. Then checking for localhost:8000/env.js figured out that it is not returning GOOGLE_CLIENT_ID. Created a new GOOGLE_CLIENT_ID and then it worked.
- After completing authentication section noticed that when signedIn the application just shows sign-In and I can perform all the operations same as a signed In user can do. But when I refresh the application then it do shows my name on the sign-in tab. This was a problem with the code in SignInNavItem.jsx file's async signIn function.
- After doing cookie domain the application was not allowing me to sign-in. Then I added http://ui.promernstack.com:8000 in auth.js and api_handler.js in const origin and did hard refresh. Then too it didn't work. Last option I tried was to create and new GOOGLE_CLIENT_ID and restarting the server and it worked.

# Chapter 13

In this chapter, we will refactor the toast code, adding new data in Mongo to explore more ways to query important results through search bar. Secondly, we also filled the empty report page as the total counts of the owner and status type. Furthermore, the delete API was built in order to facilitate deleting and undoing the issue from the application itself.

### Screen shot
![](/readme_images/CH13(1).png)
![](/readme_images/CH13(2).png)

### Problems faced while working on chapter 13
- While working with MongoDB database faced an error saying duplicate key for id_1. By deleting the index on this id and running init.mongo.js I was able to resolve this error.

# Chapter 12
This chapter focuses on server-side rendering. It does so by using complex constructs and patterns to implement rendering which generates HTML source code on server and passes it to the browser.Server-side rendering sends a rendered page to the client whose Js bundle starts the SPA framework.
### Screen shot
![](/readme_images/Ch12.png)

### Problems faced while working on chapter 12
- When I deleted index.html from the directory structure by following the steps in the book the web page was giving a message saying index.html not found. Restarting entire setup it was fixed up.

# Chapter 11
This chapter tells about React-Bootstrap, that is a css framework allowing us an easy and aesthetic way to represent the web application.

### Screen shot
![](/readme_images/CH11.png)
### Problems faced while working on chapter 11
- No problems as such.

# Chapter 10
In this chapter, we added React forms to support user input. We modified Edit page to explore forms. Secondly, we added new API's and did the CRUD operations.

### Screen shot
![](/readme_images/CH10(2).png)
![](/readme_images/CH10(1).png)

### Problems faced while working on chapter 10
- Lots of errors and places to check to put the code. Which was quite confusing.
# Chapter 9
This chapter moves forward to build SPA client-side routing.
In this chapter we set up routing for a single page application using React's router component. It describes how to connect url with the web page along with some information on using query parameters and routes to be used to perform actions on the content of the application.

### Screen shot
![](/readme_images/CH9.png)

### Problems faced while working on chapter 9
- Got an error on failed to fetch data from the server because of an issue with the brackets in schema.graphql.
- In schema.graphql Listing 9-17 the "type Issue" was gives whereas in my application "type issue" is written which was giving an error not able to identify "issue" eventually ending up resulting in app-crashed.
# Chapter 8
To begin with, this chapter focuses on re-organizing the structure of the application to make it easy for traversal.
It separate out API code from server.js into different components and same thing is done for UI codes which makes files to be loaded as modules. In addition, the chapter also modularizes the code using Webpack into deployment and bundles. Furthermore, HMR of Webpack describes how the productivity can be increased by changing modules.

### Screen shot
![](/readme_images/CH8.png)

### Problems faced while working on chapter 8
- Got favicon.ico error in developer console and then fixed it by placing rel="shortcut icon" href="#" in link tag of header section.

# Chapter 7
In this chapter, we emphasized on structuring our project into api and ui in a way that it can be in better form when application grows bigger. Furthermore, we discusses about CORS, used ESLint to impose better coding style and to check for erroneous codes/bugs.

### Screen shot
![](/readme_images/CH7(1).png)
![](/readme_images/CH7(2).png)

### Problems faced while working on chapter 7
- While performing check using ESLint got ample of errors regarding code styles and arrangement. The book has nothing mentioned in it about plugins to be used inside the editor to fix these issue.

# Chapter 6
This chapter gives basic introduction to MongoDB. It tells on how to use mongo shell and perform CRUD operations via Node.js driver followed by modifying the IssueTracker application to perform read and write on the database.

### Screen shot
![](/readme_images/CH6.png)

### Problems faced while working on chapter 6
- While installing homebrew for MongoDB on mac m1, an error encountered saying homebrew is not in your path. Resolved it by adding some line of code in ~/.zshrc file.

# Chapter 5
This chapter dives slightly deeper into back-end server-side for getting the data using APIs from Express and Node.js server with HTML files. We will use GraphQL which is a query language instead of REST here as it eases the implementation. GraphQL is a structured API standard and it has wide range of libraries and tools.

### Screen shot
![](/readme_images/CH5.png)

### Problems faced while working on chapter 5
- At the beginning of the chapter talking about GraphQL and methods of request and response, it would be more clearly understood if some code snippet have been shown in the book for better understanding.
- In the book issue type is defined as 'issue' whereas in the code listing 5-12 in
type mutation{
issueAdd(issue: IssueInputs!): Issue!
}

    its written as capital 'I' in 'Issue!' which is incorrect.

# Chapter 4
This chapter describes about React's state component that enables component to respond to user's input and other functionalities. Furthermore, it speaks on how values of state is passed down the component hierarchy.


### Screen shot

![](/readme_images/CH4.png)
### Problems faced while working on chapter 4
- No problems faced so far.

# Chapter 3
This chapter is all about building basic pieces of the application called Issue Tracker which is essentially a CRUD application. It will create a hardcode version of the main page of Issue Tracker by passing data to the children of the components  and by composing components i.e Creating classes and combining them.

### Screen shot

![](/readme_images/CH3.png)

### Problems faced while working on chapter 3
- About the borderWrap class on page 53 of book there was no listing mentioned i.e exactly it was not mentioned whether to include it or not.

# Chapter 2

This chapter tells about the basics of React to build UI components. At first we will do server-less application using React in a HTML file. It will give an overview of server-side development by using node and npm. Then it will give an idea about the node project using Express, React, HTML, babel to transpile from one language to another for older browser support and to transform JSX to JavaScript.

### Screen shot

![](/readme_images/CH2.png)

### Problems faced while working on chapter 2
- Found it difficult install nvm version 10 on mac OS.
- Eventually moving forward to this chapter it is not clearly defined where to put the code exactly.
