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
  <p> Please make sure you have the following installed:</p>
<ul>
<li>Docker Desktop to run the container of MySQL DB</li>
 <li>Node JS ver 18+</li>
 <li>MySQL Workbench, DBeaver etc.. for viewing the DB in real time</li>
  <li>Postman, Insomia etc.. for API Testing</li>
</ul>

  <p>To run this project locally, follow these steps:</p>

  <ol>
    <li>Download zipped file on Google Drive:</li>
    <li>Navigate to the project directory:</li>
    <pre>
      <code>cd your-repository</code>
    </pre>
    <li>Install the project dependencies:</li>
    <pre>
      <code>npm install
      npm i nest</code>
    </pre>
    <p>Make sure to have 2 terminals running: One for the container and a second one for running the application</p>
    <li>Run the DB container with docker compose
      <code>docker-compose up</code></li>
   <li>Connect to the DB through MySQL WorkBench or any other application and then fill in the creditinals found at the .env file</li>
    <li>Run the application after connecting to the DB:</li>
    <pre>
      <code>npm run start:dev</code>
    </pre>
  </ol>

  <p>The API should now be running locally and accessible at <a href="http://localhost:3000">http://localhost:3000</a>.
  </p>
  <p>You may test the API with Postman, Insomia and look at the changes at real time with MySQL Workbench or any other application</p>
</body>

</html>
