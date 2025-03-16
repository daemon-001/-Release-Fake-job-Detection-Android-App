# AI Fake Job Detector

![Platform](https://img.shields.io/badge/Platform-Android-green.svg)
![Kotlin](https://img.shields.io/badge/Kotlin-1.9.0-purple.svg)

An Android application built with Kotlin and Jetpack Compose that helps users identify potentially fraudulent job listings through advanced anomaly detection. The app leverages a comprehensive fake job database hosted on Supabase and integrates with OpenRouter API for intelligent text analysis and form filling.

## 📋 Features

### Fake Job Detection
- **Anomaly Detection Algorithm**: Analyzes job listings for suspicious patterns and red flags
- **Real-time Database Updates**: Syncs with Supabase to ensure the detection system stays current with the latest scam patterns
- **Comprehensive Analysis**: Evaluates multiple factors including title, salary ranges, contact email, job description, job requirements and more

### Smart Autofill
- **Copy & Paste Functionality**: Simply copy all text from any job listing webpage and paste it into the app's autofill option
- **AI-Powered Text Analysis**: Leverages OpenRouter API to categorize and extract relevant information from raw text
- **Automatic Field Population**: Instantly fills in structured fields including:
  - Job Title
  - Salary Information
  - Contact Email
  - Job Requirements
  - Job Description

### Admin Features
- **Database Management**: Admin login tab for authorized personnel
- **Perform CRUD operation in Database**: Admin can add more data or new fraud pattern or delete existing data

### User Interface
- **Material Design 3**: Modern, clean interface following latest Android design guidelines
- **Material You (Monet)**: Dynamic theming that adapts to your device's wallpaper colors
- **Responsive Layout**: Optimized for various screen sizes and orientations

## 🛠️ Technology Stack

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM (Model-View-ViewModel)
- **Database**: Supabase
- **AI Integration**: OpenRouter API
- **Theming**: Material You with Monet dynamic color system

## ⚙️ How It Works

1. **Database Synchronization**:
   - Automatically fetch the latest database at every startup. The app requires internet connection to fetch the latest fake job database from Supabase
   - Database indicators show sync status at top bar like, ⭕ = fail to load database, 🌐 = Database loaded to the app

2. **Job Analysis Process**:
   - Enter job details manually or use the autofill feature
   - The app compares the listing against known patterns in the fake job database
   - Results show confidence score and specific suspicious elements

3. **Smart Autofill Workflow**:
   - Tap the add icon at the top bar to open autofill dilogbox
   - Copy job listing text from any source
   - Paste raw text into the app
   - AI automatically extracts and categorizes information
   - Fields are populated with structured data for analysis

4. **Refresh Database and Inputfields**:
   - Tap the reload icon at the top bar
   - Refetch the latest database from the supabase server
   - All input fields are reset to initial state 

6. **Admin Functions**:
   - Tap the gear icon to goto the admin login tab and fill username and pwd
   - Authorized users can access database management tools like add or remove database item

## 🔍 Detection Algorithm

The app uses a sophisticated multi-criteria detection system that flags potential scams based on the following checks:

```kotlin
if check_job_title() risks.add("Suspicious job title")
if check_unrealistic_salary() risks.add("Unrealistic salary")
if check_suspicious_email() risks.add("Suspicious contact email domain")
if check_buzzwords() risks.add("Contains suspicious buzzwords or promises")
if check_urgency_phrases() risks.add("High-pressure or urgency tactics")
if check_red_flags() risks.add("Suspicious company indicators")
if check_payment_request() risks.add("Found payment request")
if check_job_requirements() risks.add("Suspicious job requirements")
if check_generic_discription() risks.add("Overly generic or short job description")
if check_minimal_requirements() risks.add("Minimal or vague job requirements")
```

### Detection Criteria

- **Suspicious Job Titles**: Flags titles that match patterns commonly used in scam listings
- **Unrealistic Salary**: Identifies compensation that's significantly above market rates for the position
- **Suspicious Email Domains**: Checks contact emails against a database of known scam domains
- **Buzzword Analysis**: Detects common phrases used in fraudulent listings like "get rich quick" or "unlimited earning potential"
- **Urgency Tactics**: Identifies high-pressure language designed to rush decision-making
- **Company Red Flags**: Analyzes for suspicious company indicators like lack of verifiable information
- **Payment Requests**: Flags listings that ask for payment, fees, or financial information
- **Suspicious Requirements**: Detects unusual or inappropriate job requirements
- **Generic Descriptions**: Identifies vague or unusually short job descriptions
- **Minimal Requirements**: Flags listings with suspiciously few or vague qualifications

Each detection function accesses the Supabase database to compare against known scam patterns and uses contextual analysis to determine risk levels.

## 📥 Installation

1. Download the latest APK from the [Releases](https://github.com/yourusername/ai-fake-job-detector/releases) section
2. Enable installation from unknown sources in your device settings
3. Install the app and grant required permissions

## 🔒 Privacy

- All analysis happens on-device
- OpenRouter API calls are made with minimal data sharing like only raw text that you copied for autofill
- No sensitive user information is stored or transmitted
- Database queries are anonymized

## 📱 Screenshots

![1a](https://github.com/user-attachments/assets/91280828-0070-406c-85df-2236f6cf8c35)
![2a](https://github.com/user-attachments/assets/986c6565-f347-42be-b4de-84a1a05efbc0)

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📬 Contact

For any issues or feature requests, please open an issue or reach out at: 
X: [daemon_nitesh](https://x.com/daemon_nitesh)
Insta: [mustbe_daemon](https://www.instagram.com/mustbe_daemon)
LinkedIn: [daemon001](https://www.linkedin.com/in/daemon001)
Email: [nitesh4work@gamil.com](nitesh4work@gamil.com)

---

Made with ❤️ by [Nitesh](https://github.com/daemon-001)
