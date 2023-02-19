Welcome to your new dbt project!

### Project settings
virtualenv venv
. venv/bin/activate

rehash
pip3 install dbt-core
pip3 install dbt-snowflake


### Using the starter project

Try running the following commands:
- dbt run
- dbt test


### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [chat](https://community.getdbt.com/) on Slack for live discussions and support
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices

### Usefull commands
dbt run
dbt run --full-refresh (rebuild incremental tables)


### Project structure (pipeline) - FIRST APPROACH

RAW LAYER (TABLES)    ->    STAGING LAYER (SOURCE VIEWS)    ->  CORE LAYER (DIM & FACTS TABLES)
raw_listings                src_listings (basic checks)         dim_listings_cleansed raw_hosts                   src_hosts (basic checks)            dim_hosts_cleansed
raw_reviews                 src_reviews (basic checks)          fct_reviews
                                                                dim_listings_with_hosts