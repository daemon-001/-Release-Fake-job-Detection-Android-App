# AI Fake Job Detector

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Android-green.svg)
![Kotlin](https://img.shields.io/badge/Kotlin-1.9.0-purple.svg)

An Android application built with Kotlin and Jetpack Compose that helps users identify potentially fraudulent job listings through advanced anomaly detection. The app leverages a comprehensive fake job database hosted on Supabase and integrates with OpenRouter API for intelligent text analysis and form filling.

## 📋 Features

### Fake Job Detection
- **Anomaly Detection Algorithm**: Analyzes job listings for suspicious patterns and red flags
- **Real-time Database Updates**: Syncs with Supabase to ensure the detection system stays current with the latest scam patterns
- **Comprehensive Analysis**: Evaluates multiple factors including salary ranges, job requirements, communication channels, and more

### Smart Autofill
- **Copy & Paste Functionality**: Simply copy text from any job listing webpage and paste it into the app
- **AI-Powered Text Analysis**: Leverages OpenRouter API to categorize and extract relevant information from raw text
- **Automatic Field Population**: Instantly fills in structured fields including:
  - Job Title
  - Salary Information
  - Job Requirements
  - Job Description
  - Company Details

### Admin Features
- **Database Management**: Admin login tab for authorized personnel
- **Reset Functionality**: Button to reset all fields and load the latest database
- **Email Domain Analysis**: Identifies suspicious email domains commonly associated with scams

### User Interface
- **Material Design 3**: Modern, clean interface following latest Android design guidelines
- **Material You (Monet)**: Dynamic theming that adapts to your device's wallpaper colors
- **Responsive Layout**: Optimized for various screen sizes and orientations

## 📱 Screenshots

[Screenshots to be added]

## 🛠️ Technology Stack

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM (Model-View-ViewModel)
- **Database**: Supabase
- **AI Integration**: OpenRouter API
- **Theming**: Material You with Monet dynamic color system

## ⚙️ How It Works

1. **Database Synchronization**:
   - The app requires internet connection to fetch the latest fake job database from Supabase
   - Database indicators show sync status

2. **Job Analysis Process**:
   - Enter job details manually or use the autofill feature
   - The app compares the listing against known patterns in the fake job database
   - Results show confidence score and specific suspicious elements

3. **Smart Autofill Workflow**:
   - Copy job listing text from any source
   - Paste raw text into the app
   - AI automatically extracts and categorizes information
   - Fields are populated with structured data for analysis

4. **Admin Functions**:
   - Authorized users can access database management tools
   - Email domain analysis flags potentially suspicious communication channels
   - Reset button to restore default settings and refresh database

## 📥 Installation

1. Download the latest APK from the [Releases](https://github.com/yourusername/ai-fake-job-detector/releases) section
2. Enable installation from unknown sources in your device settings
3. Install the app and grant required permissions

## 🔨 Building From Source

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-fake-job-detector.git

# Navigate to the project directory
cd ai-fake-job-detector

# Build the app
./gradlew build

# Install on connected device
./gradlew installDebug
```

## 🔒 Privacy

- All analysis happens on-device when possible
- OpenRouter API calls are made with minimal data sharing
- No sensitive user information is stored or transmitted
- Database queries are anonymized

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📬 Contact

Project Link: [https://github.com/yourusername/ai-fake-job-detector](https://github.com/yourusername/ai-fake-job-detector)

---

Made with ❤️ by [Your Name]
