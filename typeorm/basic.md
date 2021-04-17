
### Config typeorm
**obs** in this case: instalation typeorm in path, not global. I use Cli for this especif case. (yarn namescript ...)

> install typeorm 
> install db (sql, mongo or sqlite3)
>
Config ormconfig.json
> {
"type": "sqllite",
"database":"path",
"migrations:"path/**.ts",
  cli": {
    "migratinsDir":"./src/path"
  }
>}

gommand create migretions
Config in packaje.json in case use cli
> yarn typeorm migration:create -n CreateUsers


##### Up
Create / Up a database

##### Down
When i'am delete

Run created migration
> yarn typeorm migration:run 

revert 
> migration:revert
