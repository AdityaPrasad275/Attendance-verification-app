# Attendance Verification App - Attendance Marking Plan

## UI Design

### Professor Interface

- Design an intuitive interface for professors to monitor and verify student attendance.
- Display the class details, including the course name, class time, and current attendance status.
- Provide a list of enrolled students with options to mark attendance, view attendance history, and access student details.
- Include features for managing class cancellations, scheduling adjustments, and other class-related functions.

### Student Interface

- Create a user-friendly interface for students to mark their attendance.
- Display the class details, including the course name, class time, and current attendance status.
- Implement attendance marking options, such as buttons or QR code scanning, to capture entry and exit timestamps.
- Provide notifications or reminders for upcoming classes and pending attendance marking tasks.
- Include a section for students to view their attendance history, appeal attendance, and track their overall attendance percentage.

## Logic, Database Handling, and Verification

- Implement logic to validate attendance marking based on the proximity of professor and student locations during class time.
- Store attendance records in a secure and efficient database, associating them with the relevant class, student, and timestamp information.
- Use appropriate data models and database schema to manage attendance-related data efficiently.
- Implement verification mechanisms, such as comparing location coordinates or using Wi-Fi network data, to ensure accurate attendance records.
- Handle errors and exceptions during the attendance marking process to maintain data integrity and provide a smooth user experience.
- Integrate with external services or APIs for location verification, such as geolocation or Wi-Fi network APIs.
- Implement periodic synchronization or batch processing to update attendance records and handle real-time or near-real-time requirements based on your project's needs.

<details>
  <summary> <h2> In detail picture of attendance marking process</h2></summary>  
  
1. Class Session Start:  
    - When a class session begins, the instructor starts the session through the app's interface.
    - The app generates a unique session key for that particular class session, which will be used for attendance marking.
2. Attendance Marking by Students:  
    - Students attending the class open the app and navigate to the attendance marking section.
    - They enter the session key provided by the instructor to mark their attendance for that specific session.
    - The app captures the timestamp, along with the location or Wi-Fi data, as per the chosen verification methods, for both entry and exit.
3. Attendance Verification:  
    - The app validates the attendance based on the captured data and verifies if the entry and exit occurred within the correct timeframe and location boundaries.
    - The app compares the student's location or Wi-Fi data with the instructor's location data for proximity verification.
    - If the attendance is valid, the app marks the student as present for that class session.
    - Optionally, the app can provide immediate feedback to students about their attendance status.
4. Attendance Record Storage:  
    - The attendance data, including the session key, student ID, timestamps, and attendance status, is stored in the database.
    - The attendance records are associated with the corresponding class session and student in the database.
5. Attendance Analytics and Reporting:  
    - The attendance data can be utilized for generating attendance reports, calculating attendance percentages, and identifying patterns or trends.
    - Attendance analytics can provide insights to instructors and students regarding attendance patterns, missed classes, or overall attendance performance.

Technical Implementation Details:

- Implement a dedicated section in the app's user interface for attendance marking.
- Use appropriate APIs or libraries to capture location or Wi-Fi data for entry and exit verification.
- Validate timestamps to ensure entries and exits fall within the correct timeframe.
- Compare student location or Wi-Fi data with the instructor's data using proximity algorithms or techniques.
- Store attendance records in the database, associating them with the relevant class session and student.
- Implement secure data transmission between the app and the server to protect sensitive attendance information.
- Design database tables to store attendance-related information, such as class session details, student records, and attendance status.
</details>
