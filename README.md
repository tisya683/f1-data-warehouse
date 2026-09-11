# f1-data-lakehouse

Initially I wanted to create a data warehouse. However since I'm preparing of the Databricks Data Engineering Associate Exam I decided to might as well use the community edition version of the platform. This meant that I had to change my idea from creating a data warehouse to a data lakehouse as Databricks is the pioneer behind the broze/silver/medallion architecture that is very characteristic of a data lakehouse.

Next, I was having trouble deciding what data I even wanted to load. Then I realised that the ponly f1 data api I could find, the openf1api, only captures data from 2023 ownwards and the old f1 data data endpoint from "ergast f1 api' covered the sport's data starting from 1950 before retiring in 2024.

Hence I thought it be interesting to merge the historical data from ergast with newly incremental data from openf1api in my lakehouse. Hence this lakehouse will allow me to the full range of f1 data across the  allowing me to query and compare race behaviour.


## Table of Contents 
- Data Sources
- Overview of Project
- Challenges 
- Tech Stack
- Future Improvements 


## Data Sources:

**Historical Data**
Since the ergast api for f1 data between 1950 to 2024 retired in 2024, I used a kaggle dataset which contained all the data from ergast.
The link to this dataset: https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020

**Current Data**
Whereas for the current data I used the openf1 apis from : https://openf1.org
The data from this api returns 2023-current. Sicne there's an overlap with ergast for 2023 and 2024, I filtered it to only get data from 2025 ownwards


## Overview of Project:

**Phase 1**:

```mermaid
graph LR;

  



