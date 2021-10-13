# IngitDB - git versioned & branchable JSON DB hosted at GitHub

IngitDB is driven by [IngitDB GuitHub Action](https://github.com/ingitdb/ingitdb-github-action) and supports:

- multi-versioning
  - comparison between branches & versions
  - mergin of branches
  - restore to any point in a time as a new branch
- schema definition
  - check constraints
  - foreighn keys
  - views
  - triggers
- transactions
- webhooks
- REST endpoints for views and individual records
- REST API for editing

IngitDB is somewhat like static site CMS (*Hugo, Jekyll, etc.*) but a database.


## Example database

There is a publicly available IngitDB demo database - [https://github.com/ingitdb/ingitdb-demo-db](https://github.com/ingitdb/ingitdb-demo-db)

You can alsow browser data in [https://ingitdb.com/app/at/github.com/repo/ingitdb-demo-db~main@ingitdb](https://ingitdb.com/app/at/github.com/repo/ingitdb-demo-db~main@ingitdb)

It that has next sample datasets:

- [Countries](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/countries)
  - Cities 
- **ToDo**
  - [Notes](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/todo/notes)
  - [Tags](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/todo/tags)
