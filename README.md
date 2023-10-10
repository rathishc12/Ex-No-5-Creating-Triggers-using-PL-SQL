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
### Create employee table
```
CREATE TABLE employyed(
  empid NUMBER,
  empname VARCHAR2(10),
  dept VARCHAR2(10),
  salary NUMBER
);

CREATE TABLE salrr_logg (
  log_id NUMBER GENERATED ALWAYS AS IDENTITY,
  empid NUMBER,
  empname VARCHAR2(10),
  old_salary NUMBER,
  new_salary NUMBER,
  update_date DATE
);
-- Insert the values in the employee table
insert into employyed values(1,'sojo','IT',1000000);
insert into employyed values(2,'gojo','SALES',500000)
```
### Create employee table

![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/c5e425d1-b210-4b91-ba51-f81ba04cdf63)

### Create salary_log table


![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/cdf63163-7122-4839-b733-16b2abf42361)


### PLSQL Trigger code
```
-- Create the trigger
CREATE OR REPLACE TRIGGER logg_sal_update
BEFORE UPDATE ON employyed
FOR EACH ROW
BEGIN
  IF :OLD.salary != :NEW.salary THEN
    INSERT INTO sal_logg (empid, empname, old_salary, new_salary, update_date)
    VALUES (:OLD.empid, :OLD.empname, :OLD.salary, :NEW.salary, SYSDATE);
  END IF;
END;
/
-- Insert the values in the employee table
insert into employyed values(2,'Sojo','SALES',500000);
insert into employyedd values(1,'gojo','IT',1000000);

-- Update the salary of an employee
UPDATE employyed
SET salary = 600000
WHERE empid=2;
-- Display the employee table
SELECT * FROM employyed;

-- Display the salary_log table
SELECT * FROM salrr_logg;
```
### Output:
![image](https://github.com/rathishc12/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/120539398/b909f4bf-1973-4d1d-800b-9b10234191c5)



### Result:
Thus the program implemented successfully.
