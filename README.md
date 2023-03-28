# Fit-Foodie

# Fit-Foodie

A user-interactive full stack web application that provides nutrition value of food.
It accepts food photographs as input, automatically recognizes the food and outputs the nutritional information.
It also shows user there history. So that they can track their intake of each nutrient

Some Screenshots of website are attached below
Home page. It has option to scan the food:
:![Home page](https://user-images.githubusercontent.com/85441257/218382738-6b320d25-f400-4a61-9d75-c8855634fb83.png)

About us ![Home page2](https://user-images.githubusercontent.com/85441257/218383005-04429b2e-b0f0-4077-bba5-6b9dfe73b42b.png)

Here you can select file to be uploaded
![Upload page](https://user-images.githubusercontent.com/85441257/218383036-f616ba1e-0e37-4937-87e7-4dfa66c1e989.png)

It shows nutritional value of scanned food
![Nutritional value](https://user-images.githubusercontent.com/85441257/218383152-7d74018b-5cd8-40d4-bda6-438ee11e3ece.png)

All the values displayed are in milligrams:
![image](https://user-images.githubusercontent.com/85441257/228225291-8eedcebf-5d1c-4b90-a75f-724dfc20415a.png)

Monthly, weekly and year report visual representation:
![image](https://user-images.githubusercontent.com/85441257/228225776-b0114776-031d-43df-821e-e7c978dde30b.png)


Schema for the project:
![Schema](https://user-images.githubusercontent.com/85441257/218472406-07bca278-9036-474d-9a5a-20a98c88907e.png)

## To run project follow the steps given below :

Step 1)
Open mysql command line client and follow the following steps.
Paste following commands.

create database geeklogin;
use geeklogin;

create table accounts
(  
 id int auto_increment,
username varchar(50),
password varchar(60),
email varchar(100),
PRIMARY KEY (ID)
);

CREATE TABLE nutrients (
fid int PRIMARY KEY auto_increment,
fname varchar(100),
u_id int,
fat float,
carbohydrates float,
cholesterol float,
protein float,
sodium float,
time Date default (CURRENT_DATE) not null,
FOREIGN KEY (u_id) references accounts(id)
);

Step 2)
Create a .env file in the same directory and add your mysql user and mysql password with the attributes "MYSQL_USER" and "MYSQL_PASSWORD" respectively.

Step 3)
run following command in your terminal:
pip install -r requirements.txt

Step 4)
Run app.py file
