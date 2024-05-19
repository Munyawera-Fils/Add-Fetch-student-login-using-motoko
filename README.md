# Add-Fetch-student-login-using-motoko

# pre requisite : https://github.com/Munyawera-Fils/Login-with-idenity-idenity

You must created project using dfx new sample before merge this codes. this si for education purpose.

let's break down the code and explain what's going on:

# React Component (App.jsx):

This is the main React component of the application. It handles authentication, displaying the user interface, and interacting with the Internet Computer backend.
The component uses React hooks (useState and useEffect) to manage state and side effects.
It imports necessary modules from React, the Dfinity library (@dfinity/auth-client and @dfinity/agent), and the backend declaration file (example_backend).

# Authentication:

The signIn function is responsible for initiating the authentication process using the Internet Identity service. Upon successful authentication, it sets the user's identity and updates the state to indicate that the user is logged in.
The signOut function logs the user out by revoking the authentication token and updating the state accordingly.

# Data Management:

The fetchStudents function retrieves a list of students from the backend and updates the state with the fetched data.
The handleAddStudent function is triggered when the user submits the form to add a new student. It sends a request to the backend to add the new student, clears the form fields, and then 
fetches the updated list of students to reflect the changes.

# User Interface:

The UI displays a welcome message when the user is logged in, along with buttons to sign out, add a new student, and fetch the list of students.
When the "Add New Student" button is clicked, it shows a form to input the details of the new student.
The list of students is displayed below the buttons. When the user clicks the "Fetch Students" button, it fetches the list of students from the backend and displays them in a list format.

# Styling (index.scss):

This file contains styles to make the UI visually appealing and user-friendly. It defines styles for various elements such as buttons, forms, and list items.

# Internet Computer Backend (main.mo):

This is the backend canister code written in Motoko.
It defines an actor that manages a list of students (students) and provides functions to interact with this data.
The getStudents function retrieves the list of students, while the addStudent function adds a new student to the list.

