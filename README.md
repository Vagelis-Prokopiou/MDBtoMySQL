[![Build Status](https://travis-ci.org/Vaggos/MDBtoMySQL.svg?branch=develop)](https://travis-ci.org/Vaggos/MDBtoMySQL)

# MDBtoMySQL

Bash script that automates MS Access to MySQL data migration using [mdbtools](https://github.com/brianb/mdbtools).

## Aim of the project

The aim of this project, is to help the transition of Windows/Microsoft proprietary software users, to the GNU/Linux open source community.

## Usage

The script can be used interactively or non-interactively.

### Interactive usage:

```bash
bash MDBtoMySQL.sh
```

Then the user is asked for some basic input.
* The credentials of the mysql user, in order to run the queries.
* The name of the MS Access mdb (file).
* The name of the database to be created.
* Note that `localhost` is considered as the default MySQL host.

### Non-interactive usage:
```bash
bash MDBtoMySQL.sh -m db.mdb -d movies -u user -p pass
```
where
* -m  path to mdb file.
* -d  mysql database into which to import.
* -u  mysql --username parameter.
* -p  mysql --password parameter.
* -h  mysql --host parameter.
* -g  table name that requires "grep `date +%Y-%m-%d`" to save on processing time.
* -t  table names to copy. Skip to copy everything.

## Contribute

Since I cannot test every possible case of database schema, if you encounter errors with your db setup, create an issue in order to fix it and incorporate it in the project.

All development happens on the "develop" branch. Make sure to target any PRs to that branch.
