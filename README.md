# GraphQL Demo
> An introduction to GraphQL in Javascript. We implement a fake API that provides a list(array) of customers using JSON-Server and then using GraphQL to perform CRUD operations on it.

# What is GraphQL
According to the official GraphQL website, it is a query language for APIs and a runtime for fulfilling those queries with your existing data. GraphQL provides a complete and understandable description of the data in your API, gives clients the power to ask for exactly what they need and nothing more, makes it easier to evolve APIs over time, and enables powerful developer tools. 

# Project Requirements
1. Have the latest Node.js installed on your machine

# Getting Started
```bash
# Clone this repository
$ git clone https://github.com/Gichia/graphql-demo.git

# Navigate to the folder
$ cd graphql-demo

# Install the package dependencies
$ npm install

# Run the dev server
$ npm run dev

# Open Graphiql tool on your browser
http://localhost:4000/graphql
```

# Quick Start on the Basics of GraphQL
> After the Graphiql tool loads up on your browser, you can now query the data using GraphQL. Follow these steps:

1. On the left panel of the Graphiql tool on your browser, you can perform these actions by pasting the code below:

```bash
# Get all customers
{
  customers {
    name,
    email,
    age
  }
}

# Get a single customer by id
{
  customer(id: "2") {
    name,
    email
  }
}

## Mutations are a way of manipulating your data ##
# 1. Add a new customer
mutation {
  addCustomer(
    name: "Someone New",
    email: "someone@test.com",
    age: 10
  ) {
    id,
    name,
    email
  }
}

# 2. Update an existing user
mutation {
  updateCustomer(id: "2", name: "Chris Thomas") {
    id,
    name,
    email
  }
}

# 3. Delete a user (Note: Will return null since the object will have been deleted)
mutation {
  deleteCustomer(id: "2") {
    id
  }
}
```

2. We are barely scratching the surface on this demo, but you can read more on their [Official Website](http://graphql.org/ "GraphQL Website"). __Happy Coding!__

# App Info
## Version 
1.0.0

## Author
1. Peter Gichia

## Licence
MIT

# Future Development
> May include another repo with a React Frontend.
