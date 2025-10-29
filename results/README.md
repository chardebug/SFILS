# Findings

This folder contains our findings from this database project.

The findings include details about the library patrons. For example, how many from the age range 0 to 9 years used the library, how many of them were repeat patrons (can be found from total checkouts), how many renewed (can be found from total renewals).

# Performance Metrics

This folder also contains the performance values.

Did we store the data in our database appropriately?

This is meant to be a more manageable database with multiple tables. We are not simply dumping the whole Excel sheet into one giant MySQL table.

# Results

23:20:24	CREATE DATABASE SF_LibraryDB 0.016 sec

23:20:24	USE SF_LibraryDB 0.000 sec

23:20:24	CREATE TABLE ageRange 0.031 sec

23:20:24	INSERT INTO ageRange 0.015 sec

23:20:24	CREATE TABLE roleType 0.032 sec

23:20:24	INSERT INTO roleType 0.000 sec

23:20:24	CREATE TABLE patronType 0.062 sec

23:20:24	INSERT INTO patronType 0.016 sec

23:20:24	CREATE TABLE libraryType 0.031 sec

23:20:24	CREATE TABLE notificationType 0.031 sec

23:20:24	INSERT INTO 0.000 sec

23:20:24	CREATE TABLE patron 0.047 sec

23:20:24	CREATE TABLE patronStaging 0.047 sec

23:20:24	LOAD DATA LOCAL INFILE 'C:/ProgramData/MYSQL/MySQL Server 9.5/Uploads/SFPL_Data.csv' 4.703 sec

23:20:29	INSERT INTO patron 6.359 sec

23:20:35	SELECT ...	0.000 sec / 1.515 sec



