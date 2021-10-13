# IngitDB - git versioned & branchable JSON DB hosted at GitHub

IngitDB is a dynamic (*e.g. writable*) but statically hosted database driven by [IngitDB GuitHub Action](https://github.com/ingitdb/ingitdb-github-action).

IngitDB is somewhat like static site CMS (*[GitHub Pages](https://pages.github.com/), [Hugo](https://github.com/gohugoio/hugo), [Jekyll](https://github.com/jekyll/jekyll), etc.*) but a database.

## This means:

- you do not need an application layer to:
  - edit data in an IngitDB
  - query data from IngitDB
- there is no out of box access rights separation on per user/data - you either have access to the whole DB or you don't
  - You can create your own GitHub action to restrict **editing** of data
    - In future IngitDB might offer such functionality out of the box 
- users can have either `readonly` or `readwrite` permissions for a database 
- response times for reads are very low
- it is very scalable for read operations

Also it is hosted at GitHub so you basically can run it for free.

## It supports:

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

## When use and when not to use IngitDB

While IngitDB can act as a operational database it was not desined for this purpose as it would not be quick and would not scale.

It also would not be a good choice for a DB with 100s of thouthands of records. 10th of thouthands might be OK though.

IngitDB was designed and is good for:

- Keeping & providing reference data
- Settings & metadata storage
- Data entry & data collection with integrity constraints and data validation

## Example database

There is a publicly available IngitDB demo database - [https://github.com/ingitdb/ingitdb-demo-db](https://github.com/ingitdb/ingitdb-demo-db)

You can alsow view & edit IngitDB data in a [web app](https://ingitdb.com/app/at/github.com/repo/ingitdb-demo-db~main@ingitdb).

The demo database has few sample datasets:

- [**Countries**](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/countries) [[schema](https://github.com/ingitdb/ingitdb-demo-db/blob/main/.ingitdb/collections/countries/countries.json)]
  - Cities 
- **ToDo**
  - [**Notes**](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/todo/notes) [[schema](https://github.com/ingitdb/ingitdb-demo-db/blob/main/.ingitdb/collections/todo/notes/notes.json)]
  - [**Tags**](https://github.com/ingitdb/ingitdb-demo-db/tree/main/collections/todo/tags) [[schema](https://github.com/ingitdb/ingitdb-demo-db/blob/main/.ingitdb/collections/todo/tags/tags.json)]

## It's free to use and is Open Source under [MIT License](https://opensource.org/licenses/MIT)

Below repositories contains source codes of IngitDB components:

- [https://github.com/ingitdb/ingitdb-ts](https://github.com/ingitdb/ingitdb-ts) - IngitDB client in TypeScript
- [https://github.com/ingitdb/ingitdb-github-action](https://github.com/ingitdb/ingitdb-github-action) - IngitDB engine that performs actions and modifications on commits to a database
- [https://github.com/ingitdb/ingitdb-schema](https://github.com/ingitdb/ingitdb-schema) - JSON schema definition for `.ingitdb` objects

## Contributors wanted

- Have you found this project useful?
- Do you have ideas how it can be improved?

Please don't be shy and join as a contributor - pull requests are welcome!
