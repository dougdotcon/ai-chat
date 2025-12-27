# <img src="https://raw.githubusercontent.com/ksdev-pl/ai-chat/master/public/icon-192.png" alt="Logo" width="25" height="25"/> OpenAI Chat

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

🔗 **[aichat.ksdev.pl](https://aichat.ksdev.pl)**

![Screenshot](.github/screenshot.jpg)

## Overview

**OpenAI Chat** is a modern, serverless web client designed for seamless interaction with OpenAI's language models. It prioritizes user privacy by operating entirely within the browser, ensuring that no data is ever sent to a backend server.

### Key Features

*   **100% Client-Side:** No backend required. Runs directly in your browser.
*   **Enhanced Privacy:** Your API key, chat history, and settings are stored locally using IndexedDB.
*   **Markdown Support:** Rich text formatting with full Markdown rendering for code, lists, and more.
*   **Conversation History:** Persistent chat sessions saved locally.
*   **Modern UI:** Clean, responsive, and fast user interface built with Vue.js.
*   **Docker Ready:** Easy deployment with a single `docker compose` command.

## Prerequisites

*   Node.js (v18+)
*   A valid [OpenAI API Key](https://platform.openai.com/account/api-keys)

## Getting Started

### Development

1.  **Install dependencies:**
    sh
    npm install
    

2.  **Run the development server:**
    sh
    npm run dev
    

3.  Open your browser and navigate to the local URL provided (usually `http://localhost:5173`).

### Production Build

To compile and minify for production:

sh
npm run build


The built files will be available in the `dist` directory.

### Deployment with Docker

A `docker-compose.yml` file is included for easy setup.

sh
# Start the container
 docker compose up


To run on a custom port (e.g., 8080):

sh
PORT=8080 docker compose up


The application will be available at `http://localhost:5173` (or your custom port).

## Architecture & Security

*   **Serverless:** The application is a static Single Page Application (SPA). It does not have a backend API.
*   **Data Isolation:** All sensitive data is handled client-side. Communication happens directly between your browser and OpenAI's servers.
*   **State Management:** Uses the browser's `IndexedDB` for robust and asynchronous storage of chat logs and configuration.

## License

This project is open-source and licensed under the MIT License.
