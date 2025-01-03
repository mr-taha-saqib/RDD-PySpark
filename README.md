# PySpark RDD Join Operations

This guide explains the implementation of various RDD join operations using PySpark.

## Tasks

### 1. Inner Join
Perform an inner join on `emp_id` between `rdd1` and `rdd2` to obtain an RDD containing:
- Employee ID
- Employee Name
- Employee Department
- Employee Salary  

This includes only employees who exist in both `rdd1` and `rdd2`.

---

### 2. Left Outer Join
Perform a left outer join on `emp_id` between `rdd1` and `rdd2` to obtain an RDD containing:
- Employee ID
- Employee Name
- Employee Department
- Employee Salary  

This includes all employees from `rdd1` and matching employees from `rdd2`. For employees in `rdd1` without a match in `rdd2`, the employee salary should be set to `None`.

---

### 3. Total Salary Calculation
Calculate the total salary of employees in `rdd1` by:
1. Joining `rdd1` and `rdd2` on `emp_id`.
2. Multiplying `emp_salary` with `emp_experience`.

---

### 4. Maximum Salary Calculation
Find the maximum salary of employees across all records.

---

### 5. Department-Wise Total Salary
Perform an inner join on `rdd1` and `rdd2` using both `emp_id` and `dept_id`, and calculate the total salary of employees for each department.

---

### 6. Employees Without a Department
Perform a left outer join on `rdd1` and `rdd2` using both `emp_id` and `dept_id`, and identify employees who do not belong to any department.

---

## Prerequisites
- Python 3.x
- PySpark installed and configured
- Basic understanding of PySpark RDDs and join operations

## Usage
1. Set up your PySpark environment.
2. Create `rdd1` and `rdd2` with the required data.
3. Implement the above tasks step-by-step in your PySpark script.

## Example
Below is a simplified code snippet to perform an inner join:

```python
# Inner Join Example
inner_join_rdd = rdd1.join(rdd2)
inner_join_rdd.collect()
