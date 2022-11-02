# demo-wordpress-graphql

## Step 1 :: Start MySQL Database and Wordpress
```
$docker-compose up -d
$docker-compose ps

NAME                COMMAND                  SERVICE             STATUS              PORTS
db                  "docker-entrypoint.s…"   db                  running             3306/tcp, 33060/tcp
wordpress           "docker-entrypoint.s…"   wordpress           running             0.0.0.0:8000->80/tcp

$docker-compose logs --follow
```

Go to url = http://localhost:8000 to config Wordpress
* user=admin
* password=admin

## Step 2 :: Install [GraphQL API for WordPress](https://www.wpgraphql.com/)

GraphQL url POST http://localhost:8000?graphql=true
```
{
  posts {
    nodes {
      title
      id
      content
    }
  }
}
```
