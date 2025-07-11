# Data Analyst Technical Test

### Task Introduction

You are a data analyst working on a pilot programme to assess the strategic and operational value of police enforcement data for Derbyshire Police.

Your task is to prepare a dataset that enables analysis of the relationship between police 'stop and search' events and the number of officers on patrol.

Derbyshire Police has supplied some sample patrol data. You will need to combine this with their publicly available stop and search data.

We anticipate this pilot will expand to include more police forces and broader timeframes. Your code should therefore be written to support easy extension and reuse.

You will complete **four tasks** over the next **45 minutes**. You are free to write and structure your code as you see fit.

After completing tasks 1–4, you will be required to present your solution and code, explaining:

- What you did
- How you did it
- Why you made each decision

A short live coding exercise will follow your presentation.

### Important Hints:

1. You may wish to clone this GitHub repository to your local machine for easier access to the data files.
2. JSON file readers are available in R, Python, and other languages.
3. Please retain all (final) code used to complete the exercises
4. Create your script locally — you’ll share your screen later. There is no need to open a pull request or make any changes to the test repository.
5. It may be helpful to inspect the raw data files to understand their structure.

### 1. Ingest the public 'stop and search' data

You can find a copy in `raw_data` as `04_stop_and_search.json`, `05_stop_and_search.json` and `06_stop_and_search.json`. 

### 2. Load the patrol data

This is a static csv file stored in the repo at this location: `raw_data/derbyshire_patrol_data.csv`.

### 3. Clean and filter the data.

The 'stop and search' data should be filtered to only include records which:
- have a populated 'age_range' value
- resulted in an arrest (the code for an arrest is `bu-arrest`)

The patrol data must:
- Exclude any days with missing data

### 4. Create an output for the analysts

Combine the data to generate a dataset that provides the total number of 'stop and searches' and patrols occurring each day.

**Hint: You will need to format the dates in both datasets in order to successfully join them together.**

For analysis, we require a dataset containing the following data:
- The date (formatted as yyyy-mm-dd)
- The total number of patrols occurring that day
- The total number of 'stop and searches' occurring that day

Write out this data set to a new `output_data` folder in a format that can be ingested into other tools if required.

