# IngitDB - git versioned & branchable JSON DB hosted at GitHub

IngitDB is a dynamic (*e.g. writable*) but statically hosted database driven by [IngitDB GuitHub Action](https://github.com/ingitdb/ingitdb-github-action)

This means:
- you do not need an application layer to query data from IndigoDB
- there is no access rights separation on per user/data - you either have access to the whole DB or you don't
- users can have either `readonly` or `readwrite` permissions for a database 
- response times for reads are very low
- it is very scalable for read operations

Also it is hosted at GitHub so you basically can run it for free.

It supports:

- multi-versioning
  - mergin of branches
  - comparison between branches & versions
  - restore to any point in a time as a new branch
  - cherry-picking of specific changes from older version or another branch
- schema definition
  - check constraints
  - foreign keys & lookup
  - triggers
    - on insert
    - on update
    - on delete 
  - views
    - filters
    - limited number of fields
    - operators (`+`, `-`, `/`, `*`, etc.)
    - formulas (`IIF`, `LEN`, `SUBSTR`, etc.)
    - `group by` operation
      - `having` condition
      - aggregation formulas (`SUM`, `COUNT`, etc.)
- transactions
- webhooks
- REST endpoints for views and individual records
- REST API for editing

IngitDB is somewhat like static site CMS (*Hugo, Jekyll, etc.*) but a database.

## When use and when not to use IngitDB

While IngitDB can act as a operational database it was not desined for this purpose as it would not be quick and would not scale.

IngitDB was designed and is good for:

- Keeping & providing reference data
- Settings & metadata storage
- Data entry & data collection with entegrity constraints and data validation

## Example database

There is a publicly available IngitDB demo database - [https://github.com/ingitdb/ingitdb-demo-db](https://github.com/ingitdb/ingitdb-demo-db)

You can alsow browser data in [https://ingitdb.com/app/at/github.com/repo/ingitdb-demo-db~main@ingitdb](https://ingitdb.com/app/at/github.com/repo/ingitdb-demo-db~main@ingitdb)

It that has next sample datasets:

- [Countries](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/countries)
  - Cities 
- **ToDo**
  - [Notes](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/todo/notes)
  - [Tags](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/todo/tags)
