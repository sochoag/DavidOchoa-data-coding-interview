# Live Data Engineer Challenge

This project consists of the basic tools needed to solve BEON's Live Data Engineer Challenge. It contains a New York City flights dataset, a documents collection, instructions for deploying the required database (PostgreSQL), and pre-developed projects that may help you to save time.

## Set the environment

For developing the first challenge, you will need to set an ETL tool and a PostgreSQL database. You can use whatever tool you feel most comfortable in, although we provide some pre-developed projects that can help you to save time. Our examples were made using Apache Spark, Apache Beam, and dbt and you can find them inside the directories `challenge1/spark`, `challenge/beam`, `challenge/dbt`, respectively. These projects are incomplete or may contain bugs, but already have models mappings and methods for handling CSV files and database connections. Using an SQL database is the only requirement.

### Set the database

You can deploy your database using Docker and the official PostgreSQL image by using the following command.

```bash
docker run \
--name de_challenge \
-e POSTGRES_PASSWORD="Password1234**" \
-e POSTGRES_DB=dw_flights \
-v ${PWD}/init_db.sql:/docker-entrypoint-initdb.d/init_db.sql \
-p 5432:5432 \
-d postgres
```

The `init_db.sql` file will be run at database startup for creating the user for connecting to the database and creating the required tables. Once the database has started, it is ready to use with all the necessary structures.

## What does the live coding look like?

The live coding challenge is a pair programming session where we will request you to develop an ETL pipeline using whatever tool you feel most comfortable in and a small search application (prototype), solve bugs, or give code advice. You will be able to use Google and any documentation that can help you. Instructions will be provided in the live coding session.

*Please, take a look at the datasets in order to understand the data provided. It will help you to save time.*

## Requirements

- Your preferred IDE / Code Editor
- Python 3+
- SQL Client
- PostgreSQL database
- ETL tool

## Credits

The NYC Flights 2013 dataset published by [aephidayatuloh](https://www.kaggle.com/aephidayatuloh) was extracted from [Kaggle](https://www.kaggle.com/aephidayatuloh/nyc-flights-2013).