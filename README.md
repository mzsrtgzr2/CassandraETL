# Project: Data Modeling with Cassandra

## Introduction
    
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. There is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app. My role is to create an Apache Cassandra database which can create queries on song play data to answer the questions.

## Project Overview

In this project, I would be applying Data Modeling with Apache Cassandra and complete an ETL pipeline using Python. I am provided with part of the ETL pipeline that transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.

## Datasets

For this project, you'll be working with one dataset: event_data. The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:
event_data/2018-11-08-events.csv
event_data/2018-11-09-events.csv

## Project Template

The project template includes one Jupyter Notebook file, in which:
•	you will process the event_datafile_new.csv dataset to create a denormalized dataset
•	you will model the data tables keeping in mind the queries you need to run
•	you have been provided queries that you will need to model your data tables for
•	you will load the data into tables you create in Apache Cassandra and run your queries

## Project Steps

Below are steps you can follow to complete each component of this project.

### Modelling your NoSQL Database or Apache Cassandra Database
    
1.	Design tables to answer the queries outlined in the project template
2.	Write Apache Cassandra CREATE KEYSPACE and SET KEYSPACE statements
3.	Develop your CREATE statement for each of the tables to address each question
4.	Load the data with INSERT statement for each of the tables
5.	Include IF NOT EXISTS clauses in your CREATE statements to create tables only if the tables do not already exist. We recommend you also include DROP TABLE statement for each table, this way you can run drop and create tables whenever you want to reset your database and test your ETL pipeline
6.	Test by running the proper select statements with the correct WHERE clause

### Build ETL Pipeline
1.	Implement the logic in section Part I of the notebook template to iterate through each event file in event_data to process and create a new CSV file in Python
2.	Make necessary edits to Part II of the notebook template to include Apache Cassandra CREATE and INSERT three statements to load processed records into relevant tables in your data model
3.	Test by running three SELECT statements after running the queries on your database
4.	Finally, drop the tables and shutdown the cluster

## Files

<b>Cassandra_ETL.ipynb:</b> This is the final file provided in which all the queries have been written with importing the files, generating a new csv file and loading all csv files into one. All verifying the results whether all tables had been loaded accordingly as per requirement


<b>Event_Data Folder:</b> Each event file is present separately, so all the files would be combined into one into event_datafile_new.csv


## Start Cassandra docker locally

```
docker run -d --name cassandra-docker -p 9042:9042 cassandra:3.11
```