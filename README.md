```
#example.wrangler.toml


name = "hono"
main = "src/index.ts"
compatibility_date = "2023-01-01"
account_id = "$account_id"
compatibility_flags = ["nodejs_compat"]

#for dev
# [dev]
# ip = "127.0.0.1"
# port = 8081
# local_protocol = "http"


[env.$ENVIRONMENT]
vars = { ENVIRONMENT = "$ENVIRONMENT" ,BASE_URL = "$BASE_URL"}
d1_databases =[{ binding = "DB" ,database_name = "$database_name" , database_id = "$database_id" , migrations_dir = "migrationsD1" }]

# ......


```

```
npm install
npm run dev
```

```
npm run deploy
```
