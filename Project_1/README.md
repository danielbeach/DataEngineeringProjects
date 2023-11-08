### Project 1

#### Project Description
In this first Data Engineering project the idea is to setup a Data Platform
that will provide the ability to visually build a data pipeline capable of
downloading some raw TSV data, processing it, and depositing the results into
a Lake House, then displaying a Dashboard of the results.

#### Requirements

1. The data pipeline must be able to be triggered by non-Engineering persons. So there must be
a visual representation and interaction with the pipeline. (`Airflow`, `Dagster`, `Mage`, `Prefect`, etc)

2. Python is the lanaguage used.

3. The pipeline must be hardened with the ability for all the code to be unit tested.
    - Unit Tests (one Docker command to run tests)
    - Linted and Formatted. (a Bash file that will Lint and Format all the code.)

4. The ability to run the entire data pipeline locally must be provided via Docker and bash scripts.
    - Spin up the GUI of choice from above with the pipeline loaded.

5. The output must be stored in a Lake House format. (`Delta`, `Iceberg`, `Hudi`, etc.)
    - Raw data source table
    - Metrics table

6. Apache Superset Dashboard to display metrics.
    - Ability to read Lake House table with Pandas, Polars, etc and display in Superset Dashboard.

#### Details.
You data pipeline project my gather a data set, store the raw results into the Lake House,
 then run some analtyics against that raw data. The resulting metrics should be stored into
 a second Lake House table. Those metrics should be displayed in a Apache Superset Dashboard.

The TSV raw data file can be downloaded via this URL `https://zenodo.org/records/3723940/files/full_dataset.tsv?download=1`

We are interested in the metric(s) ...
    - number of tweets per hour and day.
