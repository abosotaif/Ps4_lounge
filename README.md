# Gaming Lounge System (نظام صالة الألعاب)

A comprehensive management system for a gaming lounge, featuring device tracking, session management, financial reporting, and administrative controls. Built with React and TypeScript, styled with Tailwind CSS. This project is designed to run directly in the browser without any build steps.

## Features

- **Dashboard View**: Real-time overview of all gaming devices (PlayStations) and their status (Available, Busy, Maintenance).
- **Session Management**:
  - Start new gaming sessions for available devices.
  - Choose between 'Double' or 'Quad' game types with different pricing.
  - Select 'Open Time' or 'Timed' sessions.
  - Live timer for active sessions.
  - Gracefully end sessions and calculate costs.
  - Extend timed sessions or switch to open time when the initial time is up.
- **Reporting**:
  - View daily revenue reports.
  - Filter reports by date.
  - Print reports as a PDF or HTML page.
- **Admin Panel** (Password Protected):
  - **Price Management**: Set hourly rates for different game types.
  - **Device Management**: Add new devices, delete existing ones, or change their status.
  - **Reports Management**: Delete all historical report data.
  - **UI Label Customization**: Change any text label in the application's UI.
  - **Password Management**: Update login and admin passwords.
- **User-Friendly Interface**:
  - Dark and Light mode support.
  - Fully localized in Arabic.
  - Responsive design for various screen sizes.
  - Uses `localStorage` to persist all data, so the state is saved between browser sessions.

## Tech Stack

- **Frontend**: React, TypeScript
- **Styling**: Tailwind CSS (via CDN)
- **PDF Generation**: jsPDF, jspdf-autotable
- **Build**: No build step! The project uses native browser ES Modules with an `importmap`.

## Getting Started

To run this project locally, you need a simple local web server. Modern browsers have security restrictions (CORS policy) that prevent ES Modules from loading correctly when you open the `index.html` file directly from your filesystem (`file://...`). Serving the files over HTTP is required.

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge, etc.).
- A way to run a local web server. Several simple options are listed below.

### Running the Application

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/gaming-lounge-system.git
    cd gaming-lounge-system
    ```

2.  **Start a local web server from the project directory.** Here are a few popular and easy ways:

    **Option 1: Using Python** (Python is often pre-installed on macOS and Linux)
    ```bash
    # For Python 3
    python -m http.server

    # For Python 2
    python -m SimpleHTTPServer
    ```

    **Option 2: Using Node.js and the `serve` package**
    ```bash
    # Install serve globally (only need to do this once)
    npm install -g serve

    # Run the server
    serve -s .
    ```

    **Option 3: Using the VS Code "Live Server" Extension**
    If you use Visual Studio Code, you can install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension. Once installed, just right-click on `index.html` and choose "Open with Live Server".

3.  **Open the application in your browser.**
    The server will typically start on a port like `8000`, `5000`, or `5500`. Open your browser and navigate to `http://localhost:<PORT>`, for example, `http://localhost:8000`.

## Default Credentials

The application comes with default credentials for logging in and accessing the admin panel.

- **Login Page:**
  - **Username:** `admin`
  - **Password:** `admin`

- **Admin Panel Access:**
  - **Password:** `12`

- **Admin Panel (Password Management Only):**
  - If you forget the admin password, you can use `password` to access a special view that only allows you to manage credentials.
