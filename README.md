Eliq Energy Data Platform – Home Assignment


This repository has been updated with my submission files for the home assignment, which showcase my approach to designing an energy data platform and implementing a meaningful ETL pipeline for analytical use cases.
It also includes a fully functional Streamlit dashboard for exploring and visualizing the transformed data.


Please take a look at the demo that I have hosted
**Live Demo:** [Eliq Energy Dashboard on Streamlit](https://eliq-energy-dashboard.streamlit.app/)


** 1 Data Platform Architecture**

Visuals and team structure diagrams are uploaded as images named 

Architecture - Eliq_data_platform.jpg
Tasks - Tasks_and_first_user_stories.jpg
Roadmap & Responsibilities - Implementation_team_responsibilities.jpg


 ** 2  ETL Pipeline**

 
The `ETL_Script.py`:

- **Extract**: Reads raw hourly energy data from Parquet format.
- **Transform**:
  - Expands daily arrays into hourly records.
  - Adds rich features: season, load/peak categorization, day-of-week, weekend flags.
  - Flags records with quality issues (zero, negative, missing).
  - Aggregates daily stats and adds consumption-vs-average comparisons.
- **Load**:
  - Outputs data to Parquet and CSV.
  - Generates a `report.json` with metadata and quality summaries.
 
** 3 Streamlit Dashboard **

The [Streamlit App](https://eliq-energy-dashboard.streamlit.app/) provides an interactive interface to explore the processed dataset:

- **Overview Tab**: Key KPIs and plots showing daily and hourly consumption trends.
- **Analytics Tab**: Advanced breakdowns dropdown menus(seasonal, peak/off-peak, weekday/weekend).
- **Query Tab**: Custom filtering and export(Chosen CSV for now).
- **Report Tab**: Displays processing summary, quality metrics, and system stats.
