# BMAI_Zomato-Order-Restaurant-Analysis
![Zomato-logo1](https://github.com/user-attachments/assets/91664d75-c7dc-4694-8de8-64cbff0150a7)

# Creating database and importing table datasets:

![image](https://github.com/user-attachments/assets/1f60b9bf-e9e5-4f8c-bc36-fb2160a5a472)

# Assigned Primary key, Foreign key, Unique key and updated the required datatypes for the updated table datasets using the below-mentioned types of SQL and constraints:

* **alter table | modify column | add constraint | add primary key | add foreign key | unique | references**

# ER Diagram to show the relationship between the table datasets:

![ER Diagram](https://github.com/user-attachments/assets/fdf9e0e0-0e33-4b44-8e38-9c12898591a4)

# SQL Tasks:

# Task 1: Upload Dataset into MySQL
* **Install MySQL and create a new database (ZomatoDB).**
* **Create two tables:**
  * **Zomato_Restaurants**
  * **Zomato_Orders**
* **Import the Zomato_Orders.csv and Zomato_Restaurants.csv files into MySQL.**

create database ZomatoDB;
use ZomatoDB;
select * from Zomato_Orders;
select * from Zomato_Restaurants;
desc Zomato_Orders;
desc Zomato_Restaurants;

* **Zomato Orders Table**
desc Zomato_Orders;
alter table Zomato_Orders add constraint unique_Order_ID unique (Order_ID);
alter table Zomato_Orders modify column Order_ID varchar(50);
alter table Zomato_Orders add primary key (Order_ID);
alter table Zomato_Orders modify column Restaurant_ID varchar(50);
alter table Zomato_Orders modify column Order_Date datetime;
alter table Zomato_Orders add foreign key (Restaurant_ID) references Zomato_Restaurants (Restaurant_ID);

* **Zomato Restaurant table**
desc Zomato_Restaurants;
alter table Zomato_Restaurants modify column Restaurant_ID varchar(50);
alter table Zomato_Restaurants add constraint unique_Restaurant_ID unique (Restaurant_ID);
alter table Zomato_Restaurants add primary key (Restaurant_ID);

# Power BI Tasks:
