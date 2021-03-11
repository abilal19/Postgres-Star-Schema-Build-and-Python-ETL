# Postgres-Star-Schema-Build-and-Python-ETL

# Introduction

In this context, a startup, Sparkify (music streaming app), only has JSON data of logs of user activity in terms of songs listened to and JSON metadata on the songs in their app. The startup is interested in finding a way to analyze the data on the songs being listened to by their audience. As such, this project aims to create a Postgres database schema and ETL pipeline in Python designed to optimize queries for analyzing data from the database. Therefore, this database uses a star shaped schema optimizing for higher denormalization, while maintaining data integrity. The OLAP system of this database leads to faster analytical queries to derive business insights.

## Schema for Song Play Analysis

### Fact Table
songplays - records in log data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

### Dimension Tables
users - users in the app: user_id, first_name, last_name, gender, level
songs - songs in music database: song_id, title, artist_id, year, duration
artists - artists in music database: artist_id, name, location, latitude, longitude
time - timestamps of records in songplays broken down into specific units: start_time, hour, day, week, month, year, weekday
