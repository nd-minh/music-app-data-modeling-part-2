# Database Modeling for a Music Streaming App (Part 2)

(This project presents a NoSQL database model for a music streaming app, for a design of a relational database version of the app, please refer to Part 1 [here](https://github.com/nd-minh/music-app-data-modeling). For a design of a Data Warehouse for this music app, please refer to the project [here](https://github.com/nd-minh/music-app-data-warehouse))

In this project, our aim is to design a NoSQL database, i.e., Apache Cassandra, to store relevant data from a music streaming app. We are given the data as follows.

<img src="images/image_event_datafile_new.jpg">

We will design three tables that let us perform the following three queries.

**Query 1:**

> Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4

**Query 2:**

> Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182

**Query 3:**

> 3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'

For each query, we will design one table by setting up a partition key, clustering columns, primary key, and sorting order. Details of the project are in `etl.ipynb` file.
