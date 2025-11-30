Task Manager Agent
The Task Manager Agent (TMA) is a single-file, browser-based productivity tool designed to help users track tasks and receive timely reminders. It uses vanilla JavaScript for logic, Tailwind CSS for modern styling, and leverages the browser's Notification API for system-level alerts.

•Task Scheduling: Add tasks with specific names and due dates/times.
•Real-time Reminders: Triggers a visible toast notification and a system desktop notification (if permission is granted):
o5-Minute Pre-Alert: Warns when a task is due soon.
oExact Due Time Alert: Critical alert when the task is due NOW.
•Persistence: Task data is saved locally in the browser's storage (localStorage), so tasks remain scheduled even after closing and reopening the browser.
•Responsive Design: Optimized for both desktop and mobile use.

Features

The Task Manager Agent (TMA) provides robust, time-sensitive alerting capabilities:
•Double-Layer Reminders: The application uses two distinct reminder types: an in-page Toast Notification (for when the tab is active) and a System Notification (for when the tab is minimized or in the background).
•Exact Timing: The "due NOW" alert is handled by a precise setTimeout timer, ensuring the notification triggers within milliseconds of the scheduled due time.
•Local Persistence: Tasks are saved to the browser and are automatically re-scheduled and restored when the user reopens the application.

Limitations

As a client-side, single-file application, the TMA has a few key limitations:

1.Browser Dependent: Task data is stored only in the browser's localStorage and cannot be synced across devices or browsers. Clearing browser data will delete all scheduled tasks.

2.Notification Requirement: System notifications require the user to grant explicit permission when prompted. If permission is denied, alerts will only appear as a visible toast when the tab is open.

3.Active Tab for Reliability: While system notifications work in the background, the primary logic (the JavaScript engine) relies on the browser being open. If the browser application is completely closed (not just minimized), the timers will stop.

Technology Stack & APIs
              This project is built using minimal dependencies, focusing on simplicity and browser compatibility.

Component	Technology / API	                Purpose

Frontend	HTML5,Vanilla JavaScript	Core structure and application logic.

Styling	Tailwind CSS 	Utility-first CSS framework for responsive design and modern aesthetics.

Persistence	localStorage API	Stores task data in the user's browser for persistence across sessions.

Notifications	Notification API	Triggers system-level desktop alerts, vital for background reminders.

Timers	setTimeoutand setInterval	Used for precise "due NOW" alerts and periodic "5-minute pre-alert" checks.

Initial Setup and File Preparation

1.Create Project Folder: Create a new folder on your computer for the project.
2.Save Files: Place both the index.html file (our source code) and this README.md file into that new folder.
3.Notification Requirement: Note that when the app runs, the browser will ask for Notification Permission. It is crucial to allow this for the Task Manager Agent to alert the user when the browser window is minimized or closed.

Running the Application Locally (User Manual)

The recipient of the shared repository can use either of the following methods to run the application immediately.

Method A: Direct File Open (Recommended)

This is the simplest way to run the application, as it requires no extra tools.

1.Clone/Download: Clone the repository or download the ZIP file and extract the contents.
2.Locate File: Navigate to the folder and find the index.html file.
3.Launch: Double-click index.html. It will open instantly in your default web browser (Chrome, Firefox, Edge, etc.).

Method B: Using a Simple HTTP Server (Best for Testing)

This method ensures all advanced browser features (like the Notification API) work reliably by simulating a live website environment.

1.Install Node.js: Ensure you have Node.js installed.

2.Install Server: Open the terminal and install the simple HTTP server utility globally.
Command: npm install -g http-server

How to Use the Task Manager Agent

1.Input Task: Enter the name of your task in the "Task Name" field.
2.Set Due Time: Use the datetime-local input to select the precise date and time the task is due.
3.Add Task: Click the "Add Task" button. The task will appear in the "Active Tasks" list and immediately schedule two types of reminders.
4.Manage Tasks:
oClick the Checkmark button to mark a task as completed (it will move to the bottom and be crossed out).
oClick the Trash Can button to delete the task permanently.
5.Reminders: If the application is running (even in a background tab), you will receive system desktop notifications and a red toast pop-up on the screen when tasks are due.

Potential Improvements

Future enhancements could evolve the TMA into a more robust and scalable solution:

•Cloud Persistence: Integrate a backend (e.g., Firebase, Supabase) to store data, enabling cross-device synchronization and sharing.
•Recurrence/Recurring Tasks: Add an option to schedule tasks that repeat daily, weekly, or monthly.
•User Authentication: Implement sign-in functionality to personalize task lists and improve security.
•Improved UX: Use a dedicated library for modals/toasts instead of custom CSS/JS for better accessibility and animation control.

<p>
    Check out the full video demonstration: 
    <a href="[YOUR_GOOGLE_DRIVE_SHARE_LINK](https://drive.google.com/file/d/1zLnegmUxQkxpyrDydAkFM_p1oJiiaXhi/view?usp=sharing)" target="_blank">Task Manager Agent Demo Video</a>
</p>
