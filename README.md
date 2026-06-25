# User Registration & Account Management System

A clean, responsive, client-side web application built with a three-file structure (**HTML**, **CSS**, **JavaScript**). This application allows users to register an account using structured validation rules, securely persist data locally inside the browser, and manage stored records through an integrated profile manager console.

## 🚀 Live Demo
Test the production deployment live on Vercel:  
[https://vercel.app](https://vercel.app)

---

## ✨ Features

### 🔹 Registration Form & Input Validation
* **Strict Validation Rules**: Enforces clean inputs via RegExp patterns (e.g., text-only names, valid emails, and exactly 10-digit mobile numbers).
* **Age Constraint Guard**: Restricts account setups to users who are at least 13 years old based on their selected Date of Birth.
* **Credential Matcher**: Validates strong password patterns (minimum 8 characters, containing at least one uppercase letter and one digit) and cross-checks the confirmation field.

### 🔹 Local Persistence Architecture
* **`localStorage` Matrix Engine**: Instead of overwriting global keys, the system batches accounts into a single object array string (`registeredUsers`). This setup allows you to save multiple accounts directly on the client side.

### 🔹 CRUD Profile Management Dashboard
* **Dynamic Content Loading**: Intercepts DOM trees and generates user directory cards instantly upon submission.
* **Dual-Track Context Forms**: Implements hidden identity anchors (`editUserId`) to turn your registration form into an account modifier.
* **Password Field Bypass**: Conditionally hides passkey fields when editing a user to prevent unexpected credential resets.
* **Record Erasure**: Includes an inline confirmation dialog to remove profiles safely without breaking array indexing.

---

## 🛠️ Project Structure
```text
├── index.html       # Structural layouts, form entry elements, and dashboard placeholders
├── style.css        # Visual styles, responsiveness configurations, and visibility classes
└── script.js        # Form validation scripts, localStorage pipelines, and DOM injection code
```

---

## 💻 Local Quickstart Installation

Follow these steps to spin up and test the project codebase locally:

### 1. Clone the Code Repository
```bash
git clone <your-repository-url>
cd miniproject-kappa-nine
```

### 2. Launching Locally
Since this setup runs entirely on native browser features, it requires no node dependencies or background bundle compilation:
* **Direct Execution**: Double-click `index.html` within your project folder to open it instantly inside any modern web browser.
* **Development Server (Recommended)**: Right-click inside your project workspace folder in VS Code and choose **Open with Live Server** to run it at `http://127.0.0.1:5500`.

---

## ⚙️ Architectural Workflow Deep Dive

1. **Validation Check**: When a user clicks submit, the code checks all inputs against validation formulas. If an item fails, the submission halts and displays a contextual error.
2. **Context Flag Check**: The script looks for a unique verification tracker value inside `editUserId`.
   * **If Empty (Create Mode)**: Generates a unique timestamp identity string via `Date.now().toString()`, then pushes a new record block onto the storage stack array.
   * **If Populated (Edit Mode)**: Runs an array mutation filter map match, changing old properties to the new ones without breaking other accounts.
3. **Storage Sync**: The JavaScript transforms the active array back into text strings using `JSON.stringify()`, refreshes the page layout, and resets input configurations.

---

## 🤝 Contribution Policies
1. Fork this project source tree.
2. Form your dedicated adjustments branch (`git checkout -b feature/OptimizationFeature`).
3. Commit modifications with descriptive tags (`git commit -m 'Implement OptimizationFeature details'`).
4. Push adjustments to your origin fork repo (`git push origin feature/OptimizationFeature`).
5. Open an official Pull Request review track on GitHub.
