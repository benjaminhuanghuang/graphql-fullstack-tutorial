## Install Apollo client
```
    npm i - S apollo-client-preset react-apollo graphql-tag graphql
```
- apollo-client-preset offers some convenience by bundling several packages you need when working with Apollo Client:
    - apollo-client
    - apollo-cache-inmemory
    - apollo-link
    - apollo-link-http
- react-apollo contains the bindings to use Apollo Client with React.
- graphql-tag is a GraphQL parser. Every GraphQL operation you hand over to Apollo Client will have to be parsed by the gql function.
- graphql contains Facebook’s reference implementation of GraphQL - Apollo Client uses some of its functionality as well.

## Configure ApolloClient
