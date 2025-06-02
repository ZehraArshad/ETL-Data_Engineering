# Data Engineering

### Data Architecture

Data Architcture is the blueprint that has following
- structuring data
- scheduling data
- converting it into dashboards to make sense out of it
- make decisions from those dashboards


  ### Semantic Layer

  - Aggregate data and make sense out of it
  - Has business rules, we don't concern ourselves with order id, customer id etc
 
  ### ETL VS ELT

  When we can't afford to load lots of data maybe we don't have resources thats when we ETL, ideal for small businesses


### Setting up NeonDB
- Make an account (free cloud)
- New project
- After setup Neon will show a connection string
- Like postgresql://neondb_owner:<password>@ep-xyz-pooler.us-east-2.aws.neon.tech/neondb?sslmode=require
- Hostname - > ep-xyz-pooler.us-east-2.aws.neon.tech
- Password - password
- The hostname and password will be required later on in Dbt




### Setting Up DBT 
- Make an account on DBT (free dev plan)
- New project
- Configure repo (managed option)
- make a connection and add the relevant details -> username and password from neondb
- ❗ test connection -> it should pass
- ❓ If connection doesn't pass check either connections or credentials tab in account settings
- Update yml file 

```
seeds:my_new_project:+schema: raw

```

- Run dbt see
- Upload files in seed

- Go to NeonDb and cross check the tables