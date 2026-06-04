# cjstocks

# Cloud-Native Portfolio Tracker & Authentication System

A secure, full-stack portfolio management application featuring a lightweight, responsive front-end interface integrated with a cloud-native, serverless backend. This architecture leverages Azure Functions for microservices routing, an Azure SQL database for structured relational data storage, and Azure App Services for web hosting.

## 🏗️ Architecture Overview

The application is split into a decoupled, highly scalable cloud infrastructure:
1. **Presentation Layer (Azure Web App):** A responsive, static HTML5/CSS3/ES6+ user interface optimized for quick asset delivery and clean UX.
2. **Logic Layer (Azure Functions):** A serverless API backend running asynchronous execution threads to handle authentication events (`/api/login` and `/api/register`).
3. **Data Layer (Azure SQL Backend):** A secure relational database instance managing user credentials, cryptographic hashes, and historical portfolio tracking data.

## 🚀 Key Features

* **Dynamic UI Toggling:** Single-page user journey transitioning between Login and Registration states without browser reloads.
* **Asynchronous Serverless Handshakes:** Utilizes native JavaScript `async/await` and the Fetch API to securely communicate with serverless cloud endpoints.
* **Defensive Input & DOM Validation:** Built-in validation structures and explicit DOM exception handling to ensure front-end stability.
* **Secure Token-Based Sessions:** Captures and commits JSON Web Tokens (JWT) to `localStorage` for stateful session persistence across protected routes.
* **Clean CSS3 Viewport Centering:** Implementation of modern Flexbox card formatting for cross-device responsiveness.

## 🛠️ Technical Stack

* **Front-end:** HTML5, CSS3 (Flexbox), JavaScript (ES6+)
* **Cloud Hosting & Compute:** Azure App Services (Web Pages), Azure Functions (Serverless API)
* **Database Management:** Azure SQL Database
* **State & Authentication Management:** JWT (JSON Web Tokens) & Vanilla JS DOM Manipulation

## 📋 Code Highlights

### Defensive DOM Selection & QA Compliance
The script implements explicit verification guards to protect runtime processes if target HTML hooks are missing or modified during downstream development:
```javascript
function getErrorDisplay() {
    return document.getElementById('errMsg');
}

// Verification guard before execution
if (!errorDisplay) {
    console.error("QA Alert: Element 'errMsg' missing from HTML!");
    return;
}

++++++++++++++++++++++++++++++++++++++++++++++++++++

Async/Await API Integration
Network calls are handled asynchronously with stateful button transitions (disabled during inflight requests) to ensure an optimized User Experience (UX) and prevent duplicate submission payloads:

JavaScript
const response = await fetch(`https://<your-azure-domain>${endpoint}`, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ username: user, password: pass })
});


Installation
1. Clone the repository
git clone [https://github.com/yourusername/portfolio-auth-interface.git](https://github.com/yourusername/portfolio-auth-interface.git)

2. Open login.html directly in your browser or host it via a local development server (e.g., Live Server in VS Code).
