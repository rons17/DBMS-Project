# Vaccination-Drive-DBMS-Project

## Implemented a database for Vaccination/other Health Drives with user-friendly functionalities.
## Worked on documentation (SRS), ER diagram design, Relational Model and creating schema in PostgreSQL and running some SQL queries for this database to insert, delete and retrieve information.

Intution: 

In earlier times we didn’t have enough technologies like today,pandemic situations lead to world crises and economic falls, hospitals can be flooded by patients and people would lose financial support,due to these technological limitations. All the informations were stored in simple files so information retrieval was not efficient. To overcome this a well mannered vaccine database management drive should be implemented.
---------------------------------------------------------------------------------------------------

Database:
The system will be able to manage all the details about users(personal info/vaccination status), admin(gov. officials), vaccine centers along with their locations, employees, managers of respective vaccine centers, stock of the vaccines, vaccine requirements per center, inventory details, and also other disease control drives.

---------------------------------------------------------------------------------------------------

Requirements:

User: The system should display the nearest available vaccination center from the user's area.
● The user should be able to see the list of the available vaccines/medicines and their information, also the user can update their personal details. he shd get notification about the available vaccination slots.
● The system should show the expected time for the user’s turn for the vaccination.
● features like current guidelines or news updates for users, steps for the registration procedure.


Manager:
He shd be able to see the information about the users and their respective slots which are booked.
● to check the stock of the vaccines/medicines and can order based on the requirements for
respective vaccination centers.
● to see the expected arrival time for the ordered vaccines/medicines.
● generate a list of the employees working in the center and can manipulate it.

Admin:
- to generate the details about the ordered vaccines/medicines which are requested from the manager and can manipulate with it or which admin ordered from the inventory itself.
------- As an administrator, the system should be able to prioritize the orders of the vaccines based on the requirements.
● He should be able to see the details of the managers of particular centers and the
admin should be able to manipulate it.

Employee:
updating the information about the users who are vaccinated, also the employees have the privilege to provide the certificate or vaccination report to the users who are vaccinated.

Each user can update his/her personal details.

---------------------------------------------------------------------------------------------------

Functionality:
*Administration signup
*Slot booking through the query
*Displaying the nearest available vaccination centers 
*Certification and User report
*Manager details
*Latest Guidelines and registration process
*Ordering of vaccines based on center requirements
*Displaying the nearest inventories - The system will be able to display the inventories details 	such as inventory name, inventory city, etc. based on their ascending order of distance 	from the particular administration location, which has requested the vaccine stock.
*Slot vaccine quantity updation 
*Well-managed Inventory
---------------------------------------------------------------------------------------------------

Relationships:

Tables: User, Administrator, manager, employee, slots, vaccination center, order details, inventory
PK : All table id.
-User books the slot.(1-1)(FK: slot_id)
-User get certified by employee.(1-1)(FK:center_id of employee)
-Administrator order from inventory.(n-1)
-Administrator handle order details.(1-n)(FK: admin_ID)
-Employee works at vaccination center.(1-1)(FK: cneter_ID)
-Manager works at vaccination center(1-1)(FK: cneter_ID)
-Center has vaccination slots(1-n)(FK: cneter_ID)
-Order details(FK: manager_ID, Admin_ID)


---------------------------------------------------------------------------------------------------

Normalization & Schema Refinement

Normalization to 1NF:
we stored the address in a single string. All entries are atomic.

Normalization to 2NF:
only one Primary key (not composite) are already in the 2NF form.

Normalization to 3NF
no transitive functional dependencies in the relations for the non-prime attributes

Normalization to BCNF
all the functional dependencies have a primary key(i.e prime attribute) as their left-hand
side. Also, all the foreign keys included in all the relations are the primary keys of the referenced tables.

Implement model/schema in PostgreSQL and run SQL Queries to fetch required information/data.




