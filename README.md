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
        courses they have taken. You can also filter students by year. (OPTIONAL)</li>
    <li><strong>GET /students/:student_id</strong>: Retrieve specific student's personal information and the number of
        courses they have taken. You can also filter by year. (OPTIONAL)</li>
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

<h3>Student Resource</h3>
<ul>
<li><p>Retrieve all students with courses for a specific year:</p></li>
<pre><code>GET /students?year=&lt;year&gt;</code></pre>

<li><p>Retrieve a specific student with courses for a specific year:</p></li>
<pre><code>GET /students/:student_id?year=&lt;year&gt;</code></pre>

<li><p><u></u>Create a new student:</p></li>
<pre><code>POST /students</code></pre>
<pre><code>Example request body:
{
    "firstname": "John",
    "lastname": "Doe",
    "address": "123 Main St"
}
</code></pre>

<li><p>Update a student's information:</p></li>
<pre><code>PUT /students/:student_id</code></pre>
<pre><code>
Example request body:
{
    "first_name": "Updated First Name",
    "last_name": "Updated Last Name",
    "address": "Updated Address"
}
</code></pre>

<li><p>Delete a student also his related course records:</p></li>
<pre><code>DELETE /students/:student_id</code></pre>
<br></br>
<h3>Course Resource</h3>
<li><p>Retrieve a list of all courses:</p></li>
<pre><code>GET /courses</code></pre>
 
<li><p>Retrieve information about a specific course:</p></li>
<pre><code>GET /courses/:course_name</code></pre>

<li><p>Create a new course for a student:</p></li>
<pre><code>POST /courses</code></pre>
<pre><code>Example request body:
{
    "course_name": "Mathematics",
    "year": 2023
}</code></pre>

<li><p>Update course information:</p></li>
<pre><code>PUT /courses/:course_name</code></pre>
<pre><code>Example request body:
{
    "course_name": "Updated Course Name",
    "year": 2024
}</code></pre>

<li><p>Delete a course:</p></li>
<pre><code>DELETE /courses/:course_name</code></pre>
</ul>
<h2>Installation</h2>

<p>Please make sure you have the following installed:</p>
<ul>
    <li>Docker Desktop to run the container of MySQL DB</li>
    <li>Node JS ver 18+</li>
    <li>MySQL Workbench, DBeaver etc.. for viewing the DB in real-time</li>
    <li>Postman, Insomnia etc.. for API Testing</li>
</ul>

<p>To run this project locally, follow these steps:</p>

<ol>
    <li>Download zipped file on Google Drive:</li>
    <li>Navigate to the project directory:</li>
    <pre><code>cd your-repository</code></pre>
    <li>Install the project dependencies:</li>
    <pre><code>
npm install
npm i nest
</code></pre>
    <p>Make sure to have 2 terminals running: One for the container and a second one for running the application</p>
    <li>Run the DB container with docker-compose</li>
    <pre><code>docker-compose up</code></pre>
    <li>Connect to the DB through MySQL WorkBench or any other application and then fill in the credentials found at
        the .env file</li>
    <li>Run the application after connecting to the DB:</li>
    <pre><code>npm run start:dev</code></pre>
</ol>

<p>The API should now be running locally and accessible at <a href="http://localhost:3000">http://localhost:3000</a>.
</p>
<p>After running the application the tables are generated and will be visible at MySQL WorkBench</p>
<p>You may test the API with Postman, Insomnia and look at the changes at real time with MySQL Workbench or any other
    application</p>
</body>
</html>
