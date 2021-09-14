

# 1 What data to save?

=> We will be saving data in the form of strings and numbers

=> There will be two types of data

1. A table that stores users who must be registered to post
2. A table to generate information about the poem: title, author, text, year of publication

The user's information is stored in the database but not displayed. It can be used later for sending out promotional emails.

# 2 Which types of fields would you have? Do you need dates?

The following form fields are needed. Two types of dates are needed. The date the user posted the poem is auto-generated. The user provides the publication date when posting the poem. Thus the data tree looks as follows:

-> Poem title
-> Poem Author
-> Text of Poem
-> Date posted by user
-> copyright info: publication year provided by user

# Estimate how much data will you allow to be saved

-> One has to decide whether to allow only short poems, to truncate long ones, or allow limitless length
-> Given the site is meant to let visitors enjoy the fullness of a poem, I would not limit the quantity of data
-> Poem titles and name fields as well do not need limitations as we want to maintain the original information.

# Describe the data in whatever way you find best

# Show how you would create the table(s) for your data

A. Creating databases and tables

CREATE DATABASE poetry

SHOW DATABASES
USE poetry

CREATE TABLE poem_info (
	title not null
    author_name  not null,
	body not null,
	publication_date not null
    );

CREATE TABLE poetry_users (
    name varchar(255) not null,
	email varchar(255) not null,
	location varchar(255) not null
    );

B. Editing databases

1. Change values
INSERT INTO [table_name] VALUES ([values, example: date, day, name]);
