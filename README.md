<!DOCTYPE html>
<html>

<body>

 <div align="center">
       <h1>AcademEase - Student and Course Management API</h1>
        <img src="https://i.imgur.com/FAa8Lop.png" alt="Logo" width="600" height="300">
    </div>  
<h2>Overview</h2>

  <p>The Student and Course Management API is a RESTful API built using NestJS for managing student resources,
    including their personal information and the courses they have taken each year. The API uses an SQL database with MySQL to
    store student and course data and provides various endpoints to perform operations on students and courses.</p>

  <h3>Students Resource</h3>

  <ul>
    <li><strong>GET /students</strong>: Retrieve a list of all students' personal information, including how many
      courses they have taken. You can also filter students by year.</li>
    <li><strong>GET /students/:student_id</strong>: Retrieve specific student's personal information and the number of
      courses they have taken. You can also filter by year.</li>
    <li><strong>POST /students</strong>: Create a new student.</li>
    <li><strong>PUT /students/:student_id</strong>: Update a student's personal information.</li>
    <li><strong>DELETE /students/:student_id</strong>: Delete a student and all related course records.</li>
  </ul>

  <h3>Courses Resource</h3>

  <ul>
    <li><strong>GET /courses</strong>: Retrieve a list of all courses.</li>
    <li><strong>GET /courses/:course_name</strong>: Retrieve information about a specific course.</li>
    <li><strong>POST /courses</strong>: Create a new course for a student.</li>
    <li><strong>PUT /courses/:course_name</strong>: Update course information.</li>
    <li><strong>DELETE /courses/:course_name</strong>: Delete a course.</li>
  </ul>

  <h2>API Paths</h2>

  <p>Here are the main API endpoints with examples of how to use them:</p>

  <pre>
    <code>
      Retrieve all students with courses for a specific year:

      GET /students?year=&lt;year&gt;

      Retrieve a specific student with courses for a specific year:

      GET /students/:student_id?year=&lt;year&gt;

      Create a new student:

      POST /students

      Example request body:

      {
        "first_name": "John",
        "last_name": "Doe",
        "address": "123 Main St"
      }

      Update a student's information:

      PUT /students/:student_id

      Example request body:

      {
        "first_name": "Updated First Name",
        "last_name": "Updated Last Name",
        "address": "Updated Address"
      }

      Delete a student and related course records:

      DELETE /students/:student_id

      Retrieve a list of all courses:

      GET /courses

      Retrieve information about a specific course:

      GET /courses/:course_name

      Create a new course for a student:

      POST /courses

      Example request body:

      {
        "course_name": "Mathematics",
        "year": 2023
      }

      Update course information:

      PUT /courses/:course_name

      Example request body:

      {
        "course_name": "Updated Course Name",
        "year": 2024
      }

      Delete a course:

      DELETE /courses/:course_name
    </code>
  </pre>

  <h2>Documentation</h2>

  <p>For detailed documentation on how to use the API, including request and response formats, error handling, and
    more, please refer to the <a href="link-to-your-documentation">API Documentation</a>.</p>

  <h2>Installation</h2>

  <p>To run this project locally, follow these steps:</p>

  <ol>
    <li>Clone the repository to your local machine:</li>
    <pre>
      <code>git clone https://github.com/your-username/your-repository.git</code>
    </pre>
    <li>Navigate to the project directory:</li>
    <pre>
      <code>cd your-repository</code>
    </pre>
    <li>Install the project dependencies:</li>
    <pre>
      <code>npm install</code>
    </pre>
    <li>Configure your database connection by updating the database settings in
      <code>src/config/database.config.ts</code>.</li>
    <li>Run the application:</li>
    <pre>
      <code>npm run start</code>
    </pre>
  </ol>

  <p>The API should now be running locally and accessible at <a href="http://localhost:3000">http://localhost:3000</a>.
  </p>
</body>

</html>
