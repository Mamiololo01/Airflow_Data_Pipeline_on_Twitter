# Airflow Data Pipeline on Twitter

This repository demonstrates the implementation of a data pipeline using Apache Airflow to process data from Twitter. The pipeline involves extracting tweets, transforming the data, and loading it into a data warehouse for analysis.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Architecture](#architecture)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project showcases how to build a data pipeline using Apache Airflow to handle Twitter data. The pipeline extracts tweets from the Twitter API, transforms the data into a suitable format, and loads it into a data warehouse for further analysis.

## Features

- **Data Extraction**: Extract tweets from the Twitter API.
- **Data Transformation**: Process and clean the extracted data.
- **Data Loading**: Load the transformed data into a data warehouse.
- **Scheduling**: Use Apache Airflow to schedule and manage the pipeline.

## Architecture

The architecture of the data pipeline consists of the following components:

1. **Twitter API**: Source of the data.
2. **Apache Airflow**: Orchestrates the data pipeline.
3. **Data Warehouse**: Destination for the transformed data.

```plaintext
+------------+    +---------------+    +----------------+
| Twitter API| -> | Apache Airflow| -> | Data Warehouse |
+------------+    +---------------+    +----------------+
```
### Setup and Installation

To set up and run the data pipeline, follow these steps:

### Clone the repository:

`git clone https://github.com/Mamiololo01/Airflow_Data_Pipeline_on_Twitter.git`

`cd Airflow_Data_Pipeline_on_Twitter`

### Create a virtual environment:

`python -m venv venv`

`source venv/bin/activate   # On Windows use `venv\Scripts\activate`

### Install the required packages:

`pip install -r requirements.txt`

Set up Apache Airflow:

`export AIRFLOW_HOME=$(pwd)/airflow`

`airflow db init`

### Configure the Twitter API credentials:

Create a file named twitter_credentials.json in the config directory with the following structure:

JSON
`{
  "consumer_key": "your_consumer_key",
  "consumer_secret": "your_consumer_secret",
  "access_token": "your_access_token",
  "access_token_secret": "your_access_token_secret"
}`

### Start the Airflow web server and scheduler:

`airflow webserver --port 8080`

`airflow scheduler`

### Usage

To use the data pipeline, follow these steps:

Access the Airflow web interface:

`Open a web browser and go to http://localhost:8080.`

Trigger the data pipeline DAG:

In the Airflow web interface, find the DAG named twitter_data_pipeline and trigger it manually or set a schedule.

Monitor the pipeline:

Use the Airflow web interface to monitor the progress and status of the pipeline tasks.

### Contributing

We welcome contributions to this project. Please follow these steps to contribute:

### Fork the repository:

Click the "Fork" button in the top-right corner of the repository page to create a copy of the repository in your GitHub account.

Clone the forked repository:

`git clone https://github.com/your-username/Airflow_Data_Pipeline_on_Twitter.git`

`cd Airflow_Data_Pipeline_on_Twitter`

Create a new branch:

`git checkout -b my-feature`

Make your changes:

Implement your changes or additions to the repository code. Ensure your code follows the existing code style and includes necessary documentation.

Commit and push your changes:


`git add .`

`git commit -m "Description of the changes"`

`git push origin my-feature`

Create a pull request:

Go to your forked repository on GitHub and click on the "Compare & pull request" button to create a pull request to the original repository.

### License

This project is licensed under the MIT License - see the LICENSE file for details.

