# 🚀 Social Media Data Automator

A professional Python-based automation tool designed to fetch real-time profile data from platforms like **GitHub** and **TikTok** using REST APIs and RapidAPI integration.

## 📌 Project Overview
This project demonstrates how to handle different types of APIs (Public vs. Secured) and automate the extraction of user statistics such as followers, likes, and repository counts. It serves as a practical foundation for Data Engineering and Machine Learning data collection.

## 🛠️ Tech Stack
* **Language:** Python
* **Environment:** miniconda
* **Libraries:** `requests`
* **APIs:** GitHub REST API, TikTok API (via RapidAPI)

## ⚠️ Challenges Faced & Solutions
During development, I encountered several real-world engineering challenges. Here is how I solved them:

### 1. Handling "Closed" APIs (The Bot Protection Challenge)
**Challenge:** While the GitHub API is public and easy to access, TikTok blocks direct requests from Python scripts (Error 403) to prevent bot activity.
**Solution:** I utilized **RapidAPI** as a proxy bridge and implemented **Custom Headers** with API Keys to authenticate requests and bypass security filters.

### 2. Complex JSON Data Extraction
**Challenge:** The data returned by the API was nested within deep, complex JSON structures. Finding specific attributes like "Heart Count" was difficult.
**Solution:** I used Python's dictionary indexing and the `.get()` method to navigate the JSON tree safely, ensuring the script wouldn't crash if a specific data point was missing.

### 3. Network & DNS Troubleshooting
**Challenge:** Encountered "NameResolutionError" and "getaddrinfo failed" errors where the Python environment couldn't resolve the API host.
**Solution:** I performed network diagnostics using terminal commands (ping) and adjusted the execution policies of the environment to allow script-based internet requests.

## 🚀 How to Run
1. Clone this repository.
2. Install the required dependency:
   ```bash
   pip install requests
