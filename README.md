# Employee Hub

A React-based employee management dashboard for assigning, tracking, and completing workplace tasks. Administrators can create tasks for employees, while employees can review assigned work and update its progress.

## Features

### Admin dashboard

- Admin login
- View employee task statistics
- Create and assign tasks to employees
- View all employee task activity
- Track new, accepted, completed, and failed tasks
- Log out and return to the login screen

### Employee dashboard

- Employee login
- View personal task counts
- Review newly assigned tasks
- Accept assigned tasks
- Mark tasks as completed
- Mark tasks as failed when necessary
- View task details and current status
- Persist login and task data with browser local storage

## Tech Stack

- React 18
- Vite
- Tailwind CSS
- React Context API
- JavaScript (ES modules)
- ESLint

## Project Structure

```text
employee-hub/
├── public/                         # Public static assets
├── src/
│   ├── assets/                     # Application assets
│   ├── components/
│   │   ├── Auth/
│   │   │   └── Login.jsx           # Admin and employee login form
│   │   ├── Dashboard/
│   │   │   ├── AdminDashboard.jsx # Admin task management dashboard
│   │   │   └── EmployeeDashboard.jsx # Employee task dashboard
│   │   ├── TaskList/
│   │   │   ├── TaskList.jsx        # Employee task list container
│   │   │   ├── NewTask.jsx         # New task card
│   │   │   ├── AcceptTask.jsx      # Accepted task card
│   │   │   ├── CompleteTask.jsx    # Completed task card
│   │   │   └── FailedTask.jsx      # Failed task card
│   │   └── other/
│   │       ├── Header.jsx          # Dashboard header and logout
│   │       ├── CreateTask.jsx      # Admin task creation form
│   │       ├── AllTask.jsx         # Admin task overview
│   │       └── TaskListNumbers.jsx # Task count summary cards
│   ├── context/
│   │   └── AuthProvider.jsx        # Shared employee data context
│   ├── utils/
│   │   └── localStorage.jsx        # Local storage helpers and seed data
│   ├── App.jsx                     # Authentication and role routing
│   ├── App.css                     # Application styles
│   ├── index.css                   # Global styles
│   └── main.jsx                    # React entry point
├── .gitignore
├── index.html
├── package.json
├── tailwind.config.js
├── vite.config.js
└── README.md
```

## Prerequisites

- Node.js 16 or later
- npm

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/ashukalekale/employee-Management.git
cd employee-Management
npm install
```

## Running Locally

Start the Vite development server:

```bash
npm run dev
```

Open the local URL shown in the terminal, usually `http://localhost:5173`.

## Demo Login

The application currently uses local demo authentication.

**Admin**

```text
Email: admin@me.com
Password: 123
```

Employee accounts are defined in the local seed data used by the application. Use the credentials configured in `src/utils/localStorage.jsx`.

## Task Workflow

1. Log in as an administrator or employee.
2. The administrator creates and assigns a task.
3. The employee reviews the new task.
4. The employee accepts the task.
5. The employee marks it as completed or failed.
6. Dashboards update the task counts by status.

## Production Build

Create an optimized production build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

The generated files are written to `dist/`, which is ignored by Git.

## Available Scripts

- `npm run dev` - Start the Vite development server
- `npm run build` - Create a production build
- `npm run lint` - Run ESLint checks
- `npm run preview` - Preview the production build

## Notes

- Authentication and task data are currently client-side demo data.
- Browser local storage is cleared or reset independently for each browser profile.
- For production use, connect the app to a backend API and replace demo credentials with secure authentication.

## License

ISC
