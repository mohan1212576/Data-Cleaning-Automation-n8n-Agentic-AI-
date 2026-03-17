# 🎬 n8n Movie Data Cleaning Automation

An automated n8n workflow that processes movie data from email attachments, cleans and formats the data, and sends back the cleaned version via email.

## ✨ Features

- 📧 **Email Trigger**: Automatically detects incoming emails with movie data attachments
- 📊 **Data Extraction**: Reads XLSX files from email attachments
- 🧹 **Data Cleaning**: 
  - Splits combined movie ID and name columns at first colon
  - Trims whitespace from all fields
  - Standardizes formatting
- 📁 **File Conversion**: Converts cleaned data to XLSX format
- 📨 **Auto-Reply**: Sends cleaned data back to original sender

## 🖼️ Workflow Screenshots

### 1. Complete Workflow Structure
![Workflow Overview](https://github.com/mohan1212576/Data-Cleaning-Automation-n8n-Agentic-AI-/blob/main/Main%20Workflow.png)
*The full automation workflow showing all connected nodes*

### 2. Gmail Send Configuration
![Gmail Send Node](https://github.com/mohan1212576/Data-Cleaning-Automation-n8n-Agentic-AI-/blob/main/Mail%20sending.png)
*Configuration of the final Gmail node with attachment settings*

### 3. Successful Execution Result
![Gmail Output](https://github.com/mohan1212576/Data-Cleaning-Automation-n8n-Agentic-AI-/blob/main/Cleaned%20data%20in%20mail.png)
*The cleaned data successfully received in Gmail inbox*

## 📝 How It Works

```mermaid
graph LR
    A[Email with Attachment] --> B[Gmail Trigger]
    B --> C[Extract from File]
    C --> D[Code: Clean Data]
    D --> E[Convert to XLSX]
    E --> F[Gmail: Send Reply]
    F --> G[Cleaned Data to Sender]
