Daybook

A personal productivity and timetable management web application.

Daybook is a lightweight, browser-based notebook designed to help users organize their daily schedules, manage tasks, track progress and maintain personal notes.

The application provides a simple and accessible interface for everyday planning, with local data storage and offline functionality.

---

Features

- Daily and weekly timetable management
- Task creation, editing and deletion
- Task completion tracking
- Personal notes
- Priority management
- Light and dark themes
- Drag-and-drop scheduling
- Browser notifications
- JSON data export and import
- Offline support

---

Technology Stack

Technology| Purpose
HTML5| Application structure
CSS3| Styling and responsive design
JavaScript| Application logic and interactivity
LocalStorage| Persistent browser storage
Service Worker| Offline functionality
JSON| Data backup and restoration

---

Architecture

Daybook follows a client-side application architecture.

1. Frontend

The frontend is responsible for the application's user interface and functionality.

- HTML: Defines the application structure, timetable, task forms and navigation.
- CSS: Handles visual styling, responsive layouts, themes and animations.
- JavaScript: Manages application state, user interactions, task operations and data rendering.

2. Backend

Daybook currently does not implement a traditional backend server.

Application logic runs directly in the user's browser without requiring server-side processing or API requests for its core functionality.

3. Data Storage

Browser LocalStorage is used to persist application data.

It stores:

- Timetable entries
- Task completion records
- Personal notes
- Application settings

4. Offline Functionality

A Service Worker supports offline functionality by allowing the application to use previously cached resources when network connectivity is unavailable.

---

Application Data Flow

Daybook follows a browser-based data flow.

1. User Interaction: The user creates, edits or completes a task.
2. Input Processing: JavaScript receives and processes the input.
3. State Management: The application updates its internal state.
4. Data Persistence: Application state is serialized into JSON and saved in LocalStorage.
5. Interface Rendering: JavaScript updates the user interface.
6. Data Restoration: When the application is reopened, previously stored data is loaded from LocalStorage.

This process allows users to maintain their schedules without requiring a backend database.

---

Data Management

Application data is stored locally in the user's browser.

Users can:

- Export application data as JSON files.
- Import previously exported JSON backups.
- Restore their schedules and personal information when needed.

Important: Data is not automatically synchronized between devices. Clearing browser storage may result in data loss if a backup is unavailable.

---

Security Considerations

Daybook uses browser-based storage and does not currently implement user authentication or server-side access control.

Security considerations include:

- Validate imported JSON data before processing.
- Escape user-provided content before displaying it as HTML.
- Avoid storing passwords, API keys or sensitive information in LocalStorage.
- Handle browser storage errors appropriately.
- Restrict dynamically generated HTML to trusted or properly sanitized content.

These practices help improve application reliability and reduce common client-side security risks.

---

Project Structure

The current application uses a browser-based implementation.

A possible modular structure for future development is:

Daybook/
│
├── index.html
├── css/
│   └── style.css
│
├── js/
│   ├── app.js
│   ├── tasks.js
│   ├── storage.js
│   ├── calendar.js
│   └── reminders.js
│
├── icons/
├── manifest.webmanifest
└── sw.js

This is a proposed organization for future maintainability, not necessarily the current repository structure.

---

Installation

1. Clone or download this repository.
2. Open the project folder.
3. Launch "index.html" in a browser.

For offline functionality and Service Worker support, run the application through a local development server or a supported HTTPS hosting environment.

---

Development and Future Improvements

Potential improvements include:

- Cloud synchronization
- User authentication
- Backend API integration
- Database integration
- Advanced task analytics
- Cross-device data synchronization
- Improved backup and restoration
- Automated testing
- Modular frontend architecture

These improvements can help evolve Daybook into a more scalable full-stack productivity application.

---

Project Goal

To build a simple, accessible and efficient digital notebook for everyday planning and productivity.

Daybook aims to make daily scheduling, task management and personal organization easier through a lightweight and user-friendly experience.

---

Project Releases

Daybook is maintained as a single project with multiple releases.

- Daybook v1.0: Initial release.
- Daybook v2.0: Updated release with further improvements.

Refer to the GitHub Releases section to access available versions.

---

License

Specify the applicable license before distributing or reusing this project.

---

Developed as a personal productivity application project.