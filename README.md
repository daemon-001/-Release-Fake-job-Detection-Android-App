# 🌟 AI Fake Job Detector  
**Built with Kotlin and Jetpack Compose**  

## 🚀 Overview  
AI Fake Job Detector is a powerful Android app that helps users detect fake job postings using anomaly detection. The app dynamically fetches live job data from a Supabase database and analyzes job details using OpenRouter API to identify suspicious patterns.  

---

## ✨ Key Features  
### 🔍 **Anomaly Detection for Fake Job Identification**  
- Uses AI-based anomaly detection to analyze job data and identify potential fraud.  
- Suspicious email domains and salary inconsistencies are flagged automatically.  

### 📝 **Smart Autofill with AI**  
- Copy and paste raw text from any webpage (even those that restrict web scraping).  
- The OpenRouter API processes the text and automatically fills respective fields like:  
  - **Job Title**  
  - **Salary**  
  - **Job Requirements**  
  - **Job Description**  

### 🌐 **Live Data Sync from Supabase**  
- Requires an internet connection to fetch the latest job data from the Supabase database.  
- Automatically updates the local database with the latest job indicators.  

### 🎨 **Material You Theming**  
- Built with Material 3 (Monet) theming.  
- Automatically adapts the app's color scheme to match the user's device theme.  

### 👨‍💻 **Admin Panel for Database Management**  
- Secure admin login for managing job data.  
- **Reset Button** – Clears all fields and loads the latest data from the server.  

### 📧 **Domain-based Email Detection**  
- AI will analyze job emails for suspicious domains.  
- If an email or salary is missing, the AI will skip those fields during analysis.  

---

## 🧠 **Fake Job Detection Logic**  
The app’s AI-based detection engine evaluates job listings using the following checks:  

```kotlin
fun detectFakeJob(
    jobTitle: String,
    salary: String,
    email: String,
    jobDescription: String,
    jobRequirement: String,
    context: Context
): List<String> {
    val risks = mutableListOf<String>()

    if (checkJobTitle(jobTitle, context)) risks.add("Suspicious job title")
    if (checkUnrealisticSalary(salary)) risks.add("Unrealistic salary")
    if (checkSuspiciousEmail(email, context)) risks.add("Suspicious contact email domain")
    if (checkBuzzwords(jobDescription, context)) risks.add("Contains suspicious buzzwords or promises")
    if (checkUrgencyPhrases(jobDescription, context)) risks.add("High-pressure or urgency tactics")
    if (checkRedFlags(jobDescription, context)) risks.add("Suspicious company indicators")
    if (checkPaymentRequest(jobDescription, context)) risks.add("Found payment request")
    if (checkJobRequirements(jobRequirement, context)) risks.add("Suspicious job requirements")
    if (checkGenericDescription(jobDescription)) risks.add("Overly generic or short job description")
    if (checkMinimalRequirements(jobRequirement)) risks.add("Minimal or vague job requirements")

    return risks
}
```

### ✅ **Detection Criteria:**  
1. **Suspicious Job Title** – Unusual or misleading job titles.  
2. **Unrealistic Salary** – Salary far above or below market standards.  
3. **Suspicious Email Domain** – Contact email from untrustworthy domains.  
4. **Buzzwords and Promises** – Over-the-top language and unrealistic promises.  
5. **Urgency Tactics** – High-pressure phrases like "Immediate hire" or "Apply now."  
6. **Suspicious Company Indicators** – Missing or suspicious company details.  
7. **Payment Requests** – Asking for payment for training or application.  
8. **Unusual Job Requirements** – Vague, contradictory, or suspicious job criteria.  
9. **Generic Job Description** – Overly simple or short descriptions.  
10. **Minimal Requirements** – Lack of specific qualifications or experience.  

---

## 📸 Screenshots  
*Add screenshots or GIFs here to demonstrate the app in action.*  

---

## 🛠️ **Tech Stack**  
- **Kotlin** – Primary language  
- **Jetpack Compose** – Modern UI toolkit  
- **Supabase** – Backend database  
- **OpenRouter API** – AI-powered data processing  
- **Material 3** – For dynamic theming  

---

## 🚀 **Getting Started**  
### Prerequisites  
- Android Studio (latest version)  
- Supabase account and API key  
- OpenRouter API key  

### Installation  
1. **Clone the repository**  
```bash
git clone https://github.com/your-username/ai-fake-job-detector.git
```
2. **Open in Android Studio**  
3. **Set up Supabase and OpenRouter API keys**  
4. **Build and Run**  

---

## 📌 **How to Use**  
1. Open the app.  
2. Paste the raw text from a job listing.  
3. Tap the **Autofill** button – AI will extract and populate the fields.  
4. Review the job details and let the AI detect any suspicious data.  
5. Admins can log in to update the database or reset fields.  

---

## 🏆 **Why This App Stands Out**  
✅ Real-time data analysis with anomaly detection  
✅ AI-powered autofill from unstructured text  
✅ Domain-based email fraud detection  
✅ Adaptive UI with Material You  

---

## 🤝 **Contributing**  
Contributions are welcome!  
1. Fork the repo  
2. Create a new branch (`git checkout -b feature/your-feature`)  
3. Commit changes (`git commit -m "Add your feature"`)  
4. Push to the branch (`git push origin feature/your-feature`)  
5. Open a Pull Request  

---

## 📝 **License**  
This project is licensed under the [MIT License](LICENSE).  

---

## 📧 **Contact**  
For any issues or feature requests, please open an issue or reach out at: [your-email@example.com](mailto:your-email@example.com)  

