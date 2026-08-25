The College Demo Database is a simple SQL database created to manage basic college information. 
It contains four tables: department, student, course, and enrollment. The department table stores
information about different departments using a unique department ID and department name. The 
student table stores student details such as roll number, name, email, and department ID, which
connects each student to a department. The course table stores course information, including the 
course ID, course name, and the department to which the course belongs. The enrollment table manages
the relationship between students and courses by storing the student's roll number, course ID,
semester, and grade. It uses a composite primary key consisting of roll number, course ID, and
semester. Foreign keys are used to maintain relationships between the tables. Overall, this database
demonstrates the use of primary keys, foreign keys, unique constraints, not null constraints, and 
check constraints to organize and manage college-related data efficiently.
