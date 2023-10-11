# GraphQL-Server Sample

## Starting

```shell
> go run ./server.go                                                                                                                                                                                                                                                                              2023-10-10 23:27
2023/10/10 23:27:08 connect to http://localhost:8080/ for GraphQL playground
```

ブラウザで↑のエンドポイントにアクセス

## Query samples

get todos

```graphql
query {
  todos {
    id
    text
    done
    user {
      name
    }
  }
}
```

mutation

```shelll
mutation {
  createTodo(input: {
    text: "test-create-todo"
    userId: "test-user-id"
  }){
    id
    text
    done
    user {
      id
      name
    }
  }
}
```

## Reference
- https://gqlgen.com/getting-started/

