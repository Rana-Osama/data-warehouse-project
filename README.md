# dataware-house-project

#Overview

transform data source of a faculty to staging area (STG) then from STG to data warehouse (DWH) using SSIS



#A-Business model:

Educational model (faculty)=> each student can enroll many courses and each course can have many students , each course can have many prerequisites and each prerequisite can be required for many courses , each course is taught by one or more instructors and each instructor can teach multiple courses, each student can have many financial aids  and each financial aid is taken by many students, each student can have many admissions and each admission can have many students.



#B-The grain of each fact table => 

•	Enrollment fact table: it describes the number of students enrolled in each course on daily basis.

•	 Registered courses: it describes the courses on which each student is registered and the prerequisite of each course. 

•	Attendance: it describes the attendance of the student on each course with which instructor in which hall 



#C-Define dimensions =>

•	Student dimension:  it contains the attributes related to students like student id, student name, GPA, level, status, email, address and contact number to measure the performance in each course and project in each semester.

•	Course dimension: it contains the attributes related to course like course id, course name, credit hours, course hall and course description. it also includes the department id to refer to the department which have this course to measure course enrollments and course prerequisites.

•	Department dimension: it contains the attributes related to department like department id, department name and head of department.

•	Instructor dimension: it contains the attributes related to instructor like instructor id, instructor name, instructor email to measure the instructor workload.

•	Time dimension: it contains the attributes related to time like time id, day, week, month, semester and year to analyze performance over time.

•	Prerequisite dimension: it contains the attributes related to prerequisite courses like prerequisite id, prerequisite name and prerequisite description to help students in enrollment of courses.

•	Lecture hall dimension: it contains the lecture room where student attend courses, capacity and location of the room.

•	Financial aid dimension: it contains the attributes related to financial aids for students like aid id, aid type, award amount, application status.


#D-define measure in fact tables =>

•	Students_enrolled: number or students enrolled in the course

•	Year: academic year

•	Semester: first or second semester

•	Courses_registered: number of registered courses

•	NoOfAttendees: number of students attended the course





