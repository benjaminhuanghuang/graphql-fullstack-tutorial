
- Overfetching: Downloading superfluous data
- Underfetching and the n+1 problem


## SDL (Schema Definition Language)
```
    type Person {
        name: String!
        age: Int!
        posts: [Post!]!
    }

    type Post {
        title: String!
        author: Person!
    }
```

## Fetching Data with Queries
```
    {
        allPersons(last: 2) {
            name
            age
            posts {
            title
            }
        }
    }
```

## Writing Data with Mutations
```
    // create person and return it
    mutation {
        createPerson(name: "Bob", age: 36) {
            name
            age
        }
    }
```

## Realtime Updates with Subscriptions
```
    subscription {
        newPerson {
            name
            age
        }
    }
```

## Root Type
- Query
- Mutation
- Subscription


## Resolver
    The payload of a graphQL or mutation consists of a set of fields, each of 
these fields corresponds to one function called resover.
    The purpose of each resover is to retrieve the data for its corresponding field.
```
    query {
        User(id: '123'){
            name
            friends(first: 5){
                name
                age
            }
        }
    }
```
The corresponding resovers
```
    User(id: String!): User
    name(user: User!): String!
    friends(first: Int, user: User!): [User!]!
```

## GraphQL Clients



