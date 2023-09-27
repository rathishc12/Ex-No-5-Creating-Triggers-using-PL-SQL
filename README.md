# Ex. No: 5 Creating Triggers using PL/SQL

### AIM: To create a Trigger using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create salary_log table with following attributes (log_id NUMBER GENERATED ALWAYS AS IDENTITY, empid NUMBER,empname VARCHAR(10),old_salary NUMBER,new_salary NUMBER,update_date DATE);
3. Create a trigger named as log_salary-update.
4. Inside the trigger block, Insert the values into the salary_log table whenever the salary is updated.
5. End the trigger.
6. Update the salary of an employee in employee table.
7. Whenever a salary is updated for the employee it must be logged into the salary_log table with old salary and new salary.
8. Display the employee table, salary_log table.

### Program:
![image](https://github.com/Dineshkarthick27/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120552008/f15db684-604a-46f2-a9a8-49d0b047a8fe)
### Create employee table:
![image](https://github.com/Dineshkarthick27/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120552008/1dc14288-3b5c-43c2-bbf3-b58273c46a49)
### Create salary_log table
![WhatsApp Image 2023-09-26 at 22 23 14](https://github.com/DhanushPalani/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/121594640/86466cf5-53f7-4063-9ccc-e364e7072d5e)
### PLSQL Trigger code:
![image](https://github.com/Dineshkarthick27/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120552008/ee257c7a-2e0c-435a-8614-5a007ce171d9)
### Output:
![WhatsApp Image 2023-09-26 at 22 29 52](https://github.com/DhanushPalani/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/121594640/98d6405f-b231-485b-b7c5-38e605977906)
![WhatsApp Image 2023-09-26 at 22 29 21](https://github.com/DhanushPalani/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/121594640/c1caabb7-a19c-44b3-9343-e135eafc4d07)

### Result:
 The program has been implemented successfully
