---
layout: post
title: PostgreSQL
category: Databases
---

Credentials for using PostgreSQL are available in environment variables listed below:

<table class="table table-striped table-bordered">
  <thead>
    <tr>
      <th>Name</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>DATABASE_POSTGRESQL_USERNAME</td>
      <td>runner</td>
    </tr>
    <tr>
      <td>DATABASE_POSTGRESQL_PASSWORD</td>
      <td>semaphoredb</td>
    </tr>
  </tbody>
</table>

If you need to create a PostgreSQL database manually, you can use the following
command:

```bash
createdb test_db -U $DATABASE_POSTGRESQL_USERNAME
```

Note that the `createdb` command doesn't require password, since PostgeSQL
doesn't require password for accessing a database that belongs to the PosgreSQL
user that has the same name as host operating system user, by default.

### Executing Postgres commands

Add a build command which looks something like:

```bash
psql -c "some command" -d $DATABASE_NAME_TEST -P pager
```

List of all packages and versions is available on the [supported application stack](/docs/supported-stack.html) page.

### Extensions

- [PostGIS support on Semaphore](/docs/databases/postgis.html)
