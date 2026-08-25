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

  Table                         columns(n)               Normalization            Explanation
department                  dept_ id , dept_ name            1NF              Each column contains a single value, and dept_ id uniquely 
                                                                              identifies each department.
department                  dept_ id → dept_ name         2NF / 3NF           The department name depends only on the primary key dept_ id.
student                roll_ no, name, email, dept_ id       1NF              All columns contain atomic (single) values.
student                roll_ no → name, email, dept_ id      2NF              All non-key columns fully depend on the primary key roll_ no.
student                         dept_ id                     3NF              Department details are stored separately in the department table, 
                                                                              avoiding repeated department names.
course               course_ id, course_ name, dept_ id      1NF              Each column stores a single value.
course               course_ id → course_ name, dept_ id     2NF              All non-key attributes depend fully on the primary key course_ id.
course                          dept_ id                     3NF              Department information is stored separately, reducing redundancy.
enrollment          roll_ no, course_ id, semester, grade    1NF              Each column contains a single value.
enrollment         roll_ no + course_ id + semester → grade  2NF              grade depends on the complete composite primary key.
enrollment      Student and course details stored separately 3NF              Student and course information are not repeated in the enrollment table.
