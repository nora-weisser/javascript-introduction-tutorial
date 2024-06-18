# Lesson 1.2: Setting Up the Environment

---

## Installing Node.js

### What is Node.js?
- **Node.js** is a JavaScript runtime built on Chrome's V8 JavaScript engine.
- It allows you to run JavaScript on the server side.

### Why Install Node.js?
- **Server-Side Scripting:** Run JavaScript code outside of a browser.
- **Package Management:** Use npm (Node Package Manager) to manage project dependencies.

### Installation Steps
1. **Download Node.js:**
   - Go to the [Node.js official website](https://nodejs.org/).
   - Download the recommended version for your operating system.
2. **Install Node.js:**
   - Run the installer and follow the setup instructions.
   - Verify the installation by opening a terminal and typing:
     ```bash
     node -v
     npm -v
     ```

---

## Setting Up a Code Editor (VS Code)

### Why Use VS Code?
- **User-Friendly:** Intuitive interface and extensive documentation.
- **Extensible:** Supports a wide range of extensions for added functionality.
- **Integrated Terminal:** Built-in terminal for running commands and scripts.

### Installation Steps
1. **Download VS Code:**
   - Go to the [Visual Studio Code website](https://code.visualstudio.com/).
   - Download the installer for your operating system.
2. **Install VS Code:**
   - Run the installer and follow the setup instructions.

### Basic Configuration
- **Open VS Code:**
  - Launch VS Code and open your project folder.
- **Configure settings:**
  - Go to `File > Preferences > Settings` and adjust settings as needed.
  - Add commonly used settings to your `settings.json` file:
    ```json
    {
      "editor.formatOnSave": true,
      "files.autoSave": "onWindowChange",
      "javascript.validate.enable": false
    }
    ```
