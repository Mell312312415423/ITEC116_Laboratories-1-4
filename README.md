This repository contains four separate activities focused on API development using FastAPI. Each directory corresponds to a different activity, emphasizing key aspects of API creation, logical structuring, and implementation.

Folder Organization:
lab1-main/
lab2-main/
lab3-main/
lab4-main/
Each folder holds the codebase for its respective activity. Below is an overview of each activity and its objectives.

Activity 1: Factorial API
Objectives:
Introduce FastAPI as a framework for building APIs.
Reinforce Python skills in API development.
Implement, execute, and test APIs using FastAPI.
Develop logical thinking and technical proficiency.
Description:
In this activity, we created an API that calculates the factorial of a given number using FastAPI. The API adheres to the following requirements:

Endpoint: /factorial/{starting_number}
Logic:
Computes the factorial of the input number.
If the input is 0, the API responds with { "result": false }.
The computation utilizes a while loop.
Example Requests:
GET /factorial/5 → { "result": 120 }
GET /factorial/0 → { "result": false }
This implementation showcases fundamental API development principles while ensuring efficient computation.

Activity 2: To-Do List API
Objectives:
Understand different API parameterization methods.
Explore HTTP methods and best practices.
Implement a simple CRUD API.
Description:
This activity involves creating a To-Do List API in FastAPI with the following specifications:

Initial Data:

python
Copy
Edit
task_db = [
    {"task_id": 1, "task_title": "Laboratory Activity", "task_desc": "Create Lab Act 2", "is_finished": False}
]
Endpoints:

GET /tasks/{task_id} – Retrieve a specific task.
POST /tasks – Add a new task.
PATCH /tasks/{task_id} – Modify an existing task.
DELETE /tasks/{task_id} – Remove a task.
Response Handling:

Successful operations return { "status": "ok" }.
Errors return { "error": <error_message> }.
Validation Measures:

Prevents null values and negative numbers.
Handles invalid inputs such as division by zero.
This activity highlights API parameterization, HTTP methods, and CRUD best practices.

Activity 3: JSON Handling API
Objectives:
Understand JSON as a fundamental data format in API development.
Parse JSON data and navigate structures in Python.
Convert Python data into valid JSON formats.
Description:
Here, we built an API that retrieves user posts along with related comments using JSON data.

Setup Steps:

Clone the repository.
Navigate to the lab3 directory.
Set up a virtual environment and install dependencies.
Endpoint:

GET /detailed_post/{userID} – Fetches all posts and comments associated with a given user ID.
Functionality:

Retrieves posts for the specified user.
Includes all associated comments for each post.
Uses appropriate key-value structures in the response.
Expected output can be found in the expected_output.json file within the repository. This activity reinforces efficient JSON handling and structured API responses.

Activity 4: API Versioning, Authentication, and Error Handling
Objectives:
Implement API versioning, authentication, and proper error handling.
Follow best practices for managing environment variables securely.
Description:
This activity extends the To-Do List API from Activity 2 by adding:

Versioning:

First version: apiv1
Updated version: apiv2
Error Handling:

404 Not Found for non-existent tasks.
201 Created for successful additions.
204 No Content for successful updates/deletions.
200 OK for all other cases.
Authentication:

Requires an API key for access.
The API key is stored in a .env file (excluded from the repository via .gitignore).
Required Output:
A GitHub repository containing:

Updated API with versioning, authentication, and error handling.
.gitignore to exclude .env files.
API key stored securely and shared privately.
This activity focuses on enhancing security, scalability, and best practices in API development.

Setup Instructions for All Activities
Install dependencies:
sh
Copy
Edit
pip install fastapi uvicorn python-dotenv
Navigate to the specific activity folder.
Run the FastAPI server:
sh
Copy
Edit
uvicorn main:app --reload
Access API documentation at:
http://127.0.0.1:8000/docs
127.0.0.1
