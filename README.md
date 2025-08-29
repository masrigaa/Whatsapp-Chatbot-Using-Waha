# n8n WhatsApp Chatbot with Waha - Outputs Archive

[![GitHub last commit](https://img.shields.io/github/last-commit/masrigaa/n8n-Whatsapp-Chatbot-Using-waha?style=for-the-badge&label=Last%20Update)](https://github.com/masrigaa/n8n-Whatsapp-Chatbot-Using-waha)
[![GitHub repo size](https://img.shields.io/github/repo-size/masrigaa/n8n-Whatsapp-Chatbot-Using-waha?style=for-the-badge&label=Repo%20Size)](https://github.com/masrigaa/n8n-Whatsapp-Chatbot-Using-waha)

---

## 🚀 Overview

This repository serves as a centralized and version-controlled archive for all outputs and results generated from various [n8n](https://n8n.io/) automation workflows. Specifically, it focuses on storing data and artifacts related to our **WhatsApp Chatbot built using Waha**.

The main purpose is to provide an accessible and traceable history of workflow executions, facilitating easier review, debugging, and monitoring of the chatbot's operational performance.

## 🔧 Setup & Configuration

To effectively utilize and run the n8n workflows for the WhatsApp Chatbot, please ensure you have completed the following setup steps:

### 1. Prerequisites

Before you begin, make sure you have:
*   **n8n Instance**: A running instance of n8n (self-hosted or cloud).
*   **Waha Instance**: A deployed and running [Waha](https://waha.devlike.pro) instance. Waha acts as the bridge between WhatsApp and your n8n workflows.
*   **WhatsApp Number**: An active WhatsApp phone number connected to your Waha instance.

### 2. Import n8n Workflows

*   Import the relevant n8n workflow JSON files (e.g., from a `workflows/` directory in a companion repository, or directly into your n8n instance).

### 3. Configure Credentials

*   **Waha Credentials**: In n8n, you will need to set up credentials for connecting to your Waha instance. This typically involves providing:
    *   **Waha Base URL**: The URL of your running Waha instance.
    *   **Waha Token (if applicable)**: Any API token or key required by your Waha setup for authentication.
*   **Other Service Credentials**: Configure any other necessary credentials for services integrated into your n8n workflows (e.g., database, external APIs, etc.).

### 4. Replace Localhost with Public Waha Link

**Crucial Step**: If your n8n workflow was developed using a local Waha instance, you must update all Waha HTTP Request nodes (or any nodes interacting with Waha) to point to your **publicly accessible Waha instance URL**.

*   Navigate through your n8n workflows.
*   Identify any nodes making requests to `http://localhost:3000` (or similar local addresses).
*   Replace these `localhost` URLs with the **actual public URL** where your Waha instance is deployed (e.g., `https://your-waha-instance.com`). This ensures your n8n instance can communicate with Waha even when deployed remotely or when n8n itself is not running locally.

## 🖼️ Workflow Visual Example

Below is a visual representation of an n8n workflow. While the full workflow definitions are available as JSON files, these screenshots offer a quick way to understand the workflow's logic and design at a glance.

<p align="center">
  <img width="800" alt="Example n8n Workflow" src="https://cdn.discordapp.com/attachments/1011316700316192839/1410963679783944272/Screenshot_2025-08-29_190315.png?ex=68b2edd3&is=68b19c53&hm=7f9a967e7f60e0b11cebf8dc56c1cf1e21766c15dc5bc0770e69235b6ddefe14" />
</p>

## ⚙️ How Outputs Are Generated

Our n8n workflows are configured to automatically push their relevant outputs directly into this repository. This integration is typically achieved using n8n's built-in Git capabilities or via custom scripts that handle the commit and push operations to this GitHub repository.

## ➡️ Accessing Outputs

You can easily browse all stored files directly on GitHub, or clone the repository to your local machine for offline access and analysis:

<pre>git clone https://github.com/masrigaq/n8n-Whatsapp-Chatbot-Using-waha.git 
cd n8n-Whatsapp-Chatbot-Using-waha
</pre>

## ✨ Contribution & Workflow Integration Guidelines

If you are developing a new n8n workflow, or modifying an existing one, and wish for its outputs to be stored here, please adhere to the following guidelines:

1.  **Dedicated Subdirectory**: Create a unique subdirectory for your workflow within the repository.
2.  **Clear Naming Conventions**: Ensure outputs are clearly named and dated (e.g., `[workflow-name]_YYYYMMDD_HHMMSS.[ext]`).
3.  **Sensitive Data Handling**: Be mindful of sensitive information; ensure it is properly handled and **not** committed directly to the repository.

For any questions regarding workflow integration or repository structure, please feel free to reach out to the maintainer.

## 👨‍💻 Developed & Maintained By

This repository is developed and maintained by:

-   **Asla Fikri**
    -   [GitHub](https://github.com/masrigaa)
    -   [LinkedIn](https://www.linkedin.com/in/aslamul-fikri-alfirdausi)

---
