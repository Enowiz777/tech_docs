# GraphQL

# References:
- Learn GraphQL: https://graphql.org/learn/

# 1. Introduction

## *What is GraphQL?*
GraphQL is a query language for your API, and a server-side runtime for executing queries using a type system you define for your data. GraphQL isn't tied to any specific database or storage engine and is instead backed by your existing code and data.

## *How does GraphQL work?*

A GraphQL service is created by defining types and fields on those types, then providing functions for each field on each type. For example, a GraphQL service that tells you who the logged in user is (me) as well as that user's name might look like this:

```js
type Query {
  me: User
}

type User {
  id: ID
  name: String
}
```
Functions for each field on each type:
```js
function Query_me(request) {
  return request.auth.user;
}

function User_name(user) {
  return user.getName();
}
```
Query examples:
Input:
```js
{
  me {
    name
  }
}
```

JSON result:
```js
{
  "me": {
    "name": "Luke Skywalker"
  }
}
```