# What I learned 


## DATABASE NORMALIZATION

![normal](https://res.cloudinary.com/practicaldev/image/fetch/s--rDPLIrdR--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://cdn.filestackcontent.com/SGIy2EgRQN4f28VaUYBS)


* What is normalization ?
Normalization is a technique for organizing data in a database.


* It is important that a database is normalized to minimize redundancy (duplicate data) and to ensure only related data is stored in each table.

* It also prevents any issues stemming from database modifications such as insertions, deletions, and updates.
* The stages of organization are called normal forms.



* First Normal Form (1NF):
    - Data is stored in tables with rows uniquely identified by a primary key
    - Data within each table is stored in individual columns in its most reduced form
    - There are no repeating groups


* Second Normal Form (2NF):
    - Everything from 1NF
    - Only data that relates to a table’s primary key is stored in each table

* Third Normal Form (3NF):
    - Everything from 2NF
    - There are no in-table dependencies between the columns in each table



