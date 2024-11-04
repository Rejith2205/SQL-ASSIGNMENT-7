## SQL-ASSIGNMENT-7
### **1.	Add a new column called DOB in Persons table with data type as Date.**
*ALTER TABLE PERSONS ADD DOB date;*
### **2.	Write a user-defined function to calculate age using DOB.**

  *DELIMITER $$  
Create function customer_age(DOB date)  
returns int   
DETERMINISTIC   
Begin   
	Declare age int;   
	Set AGE = year(curdate())-year(DOB);  
	Return age;  
End $$*

### **3.	Write a select query to fetch the Age of all persons using the function that has been created.** 
*select customer_age(DOB) from persons;*
### **4.	Find the length of each country name in the Country table.**
*select country_name,area from country;*

