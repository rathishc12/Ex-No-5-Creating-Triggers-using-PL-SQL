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
![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/ed7ba578-491c-4f3a-a64b-49d912f6d9a1)
### Create employee table:
![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/9bffa33b-11fc-406f-b436-20d259bf40aa)
### Create salary_log table
![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/ccd4991d-05eb-4ea0-b167-8327ca251928)
### PLSQL Trigger code:
![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/68c5c758-41ed-4718-8dc3-77e566831c21)
### Output:
![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/d26537d8-4b04-4b1d-b1e9-15153d79e919)
![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/e974b13b-0b72-41bc-9d7a-2b9c583ebf6f)

### Result:
 The program has been implemented successfully
