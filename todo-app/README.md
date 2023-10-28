# GraphQL-Server Sample

## Feature

|status|featuer|
|:---:|:---|
|🔲|データベースに接続する|
|🔲||

## Starting

```shell
> go run ./server.g
2023/10/10 23:27:08 connect to http://localhost:8080/ for GraphQL playground
```

ブラウザで↑のエンドポイントにアクセス


Portを変えて実行する場合は、

```shell
> PORT=10000 go run ./server.go
2023/10/10 23:27:08 connect to http://localhost:10000/ for GraphQL playground
```


## Query samples

get todos

```graphql
query {
  todos {
    id
    title
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
    title: "test-create-todo"
    userId: "test-user-id"
  }){
    id
    title
    done
    user {
      id
      name
    }
  }
}
```


## schema.graphqlからモデルなど自動生成

```shell
gqlgen generate
```

## Reference
- https://gqlgen.com/getting-started/
