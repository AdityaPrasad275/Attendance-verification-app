# Attendance Verification App - Class Creation Plan

## UI Design

### Professor Interface

- Design an intuitive interface for professors to create and manage classes.
- Include forms or input fields for class details such as course code, class name, schedule, and attendance requirements.
- Provide options for adjusting class schedules, canceling classes, or making other modifications.
- Display a list of enrolled students and options to manage student enrollment within each class.
- Implement functionality to instantiate all classes for a semester at once, reducing manual effort.

### Student Interface

- Create a user-friendly interface for students to view available classes and enroll in courses.
- Implement search and filtering options to help students find classes based on course code, name, or other criteria.
- Display class details, including the course name, schedule, professor information, and availability status.
- Provide an enrollment mechanism, such as a button or link, for students to join classes of interest.
- Include a feature that allows students to see all the classes they are enrolled in for the semester.

## Logic, Database Handling, and Verification

- Implement logic to validate class creation, ensuring that required information is provided and meeting any constraints or prerequisites.
- Store class data in a secure and efficient database, associating it with relevant course and instructor information.
- Use appropriate data models and database schema to manage class-related data efficiently.
- Implement verification mechanisms, such as checking for class conflicts with existing schedules, to ensure accurate and conflict-free class creation.
- Handle errors and exceptions during the class creation process to maintain data integrity and provide a smooth user experience.
- Integrate with external services or APIs, if necessary, for additional verification or validation.
- Implement functionality for professors to add extra classes, allowing flexibility in the schedule.
- Include options for professors to cancel classes if necessary, with appropriate attendance implications.
- Develop a feature that allows students to view all the classes they are enrolled in for the semester, providing an overview of their course schedule.


<details>
  <summary><h1>Slightly more verbose and indepth explanation</h1></summary>
  
1. Instructor's Perspective:
    - Instructors will have access to a dedicated interface within the app to create and manage courses.
    - Upon logging in, instructors can navigate to the course creation section.
    - Instructors will input details such as course name, course ID, class timings, location, and other relevant information.
    - After submitting the course creation form, the app will generate a unique course ID and store the course details in the database.
    - Instructors can view and manage their courses, including adding or canceling classes within each course, through the instructor interface.
    - When an instructor adds a new class to a course or cancels an existing class, the corresponding class session details are stored or removed from the "classes" table in the database.
3. Student's Perspective:
    - Students will have access to their own interface within the app to view and enroll in available courses.
    - In the student interface, they can browse or search for courses and view their corresponding class schedules.
    - Students can select the desired courses and enroll in them by adding them to their course list.
    - When a student enrolls in a course, the app will associate the student ID with the corresponding course ID in the "enrollments" table in the database.
    - Students will receive notifications or reminders for upcoming classes based on their enrolled courses.
    - Within each enrolled course, students can view the class sessions and their respective details, such as date, time, location, and attendance status.
4. Integration with the Database:
    - The database will contain tables for "courses," "classes," "instructors," "students," and an "enrollments" relationship table.
    - The "courses" table will store course information, including course name, course ID, and other relevant details.
    - The "classes" table will store class session details, such as class date, time, location, and course ID as a foreign key.
    - The "instructors" table will store instructor information, while the "students" table will store student information.
    - The "enrollments" table will establish the association between students and courses by linking the student IDs with the corresponding course IDs.
    - When an instructor creates a course, a new record is inserted into the "courses" table, and relevant information is updated in the "instructors" table.
    - When an instructor adds or cancels a class within a course, the corresponding class session details are added or removed from the "classes" table.
    - When a student enrolls in a course, a new record is inserted into the "enrollments" table, linking the student ID to the corresponding course ID.
</details>
