# 🤖 AI Job Email Assistant

An AI-powered email management system that automatically identifies, categorizes, and extracts important job-related information from Gmail using Artificial Intelligence.

## 📌 Project Overview

The **AI Job Email Assistant** is designed to simplify the job search process by automatically analyzing emails and identifying important recruitment updates.

It uses the Gmail API to fetch emails and Google Gemini AI to classify them into different categories, such as job opportunities, interview invitations, assessments, and irrelevant emails.

The system extracts useful information such as company name, job title, interview date, assessment deadline, and application status, helping job seekers manage their applications efficiently.

## 🎯 Key Features

- **Automatic Email Fetching:** Fetch emails directly from Gmail using Gmail API.
- **AI-Based Email Classification:** Uses Google Gemini AI to identify job-related emails.
- **Email Categorization:** Classifies emails into:
  - JOB_OPPORTUNITY
  - INTERVIEW
  - ASSESSMENT
  - IGNORE
- **Information Extraction:** Extracts:
  - Company Name
  - Job Title
  - Job Location
  - Interview Date and Time
  - Assessment Deadline
  - Application Status
  - Job Application URL
- **Database Management:** Stores processed email information using SQLite.
- **Duplicate Prevention:** Avoids processing previously analyzed emails.
- **Dashboard:** Displays categorized job emails and application information.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend development |
| Gmail API | Fetching emails |
| Google Gemini AI | Email classification |
| SQLite | Database management |
| Flask | Backend API |
| Pandas | Data processing |
| HTML, CSS | Dashboard interface |

## ⚙️ Project Workflow

1. Connect to Gmail using Google OAuth 2.0.
2. Fetch emails from the Gmail inbox.
3. Extract email subject and body.
4. Send email content to Gemini AI.
5. Classify emails into predefined categories.
6. Extract important job-related information.
7. Store the results in an SQLite database.
8. Display categorized emails through a dashboard.

## 📂 Project Structure

```text
AI-Job-Email-Assistant/
│
├── credentials/
│   └── credentials.json
│
├── database/
│   └── database.py
│
├── ai_classifier.py
├── gmail_fetcher.py
├── main.py
├── app.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

*Note: Adjust the folder structure according to your final implementation.*

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/AI-Job-Email-Assistant.git

cd AI-Job-Email-Assistant
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows:**
```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Google Gemini API

- Create an API key through Google AI Studio.
- Add the key to your `.env` file.

```env
GEMINI_API_KEY=your_api_key_here
```

### 5. Configure Gmail API

- Open Google Cloud Console.
- Enable Gmail API.
- Configure OAuth consent screen.
- Create OAuth client credentials.
- Download the credentials JSON file.
- Place it inside the `credentials` folder.

### 6. Run the Project

```bash
python main.py
```

For the Flask dashboard, if configured:

```bash
python app.py
```

## 📊 Sample AI Classification Output

```json
{
  "is_job_related": true,
  "category": "INTERVIEW",
  "company_name": "Deloitte",
  "job_title": "Data Analyst",
  "location": "Mumbai",
  "interview_date": "2026-11-20",
  "assessment_deadline": null,
  "application_status": "Interview Scheduled",
  "job_url": "https://example.com/job"
}
```

*Example output for demonstration purposes.*

## 🔮 Future Enhancements

- Automated interview reminders.
- Job application tracking.
- Assessment deadline notifications.
- Advanced job search dashboard.
- Resume matching with job descriptions.
- Integration with additional job portals.

## 🔐 Security

- Gmail access is managed through OAuth 2.0.
- API keys are stored in environment variables.
- Credentials and sensitive information should not be uploaded to GitHub.
- Use `.gitignore` to protect confidential files.

## 💡 Project Objective

The main objective of this project is to reduce the manual effort involved in managing job application emails by using AI-based automation, making the job search process more organized and efficient.

## 👩‍💻 Author

**Your Name**

Aspiring Data Analyst | Python | SQL | Data Science | AI & Machine Learning

---

⭐ If you find this project useful, consider giving it a star on GitHub!
