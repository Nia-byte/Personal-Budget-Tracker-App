# ZakaZaka Budget Management App
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Android-green.svg)
![Kotlin](https://img.shields.io/badge/kotlin-1.9+-purple.svg)
![MinSDK](https://img.shields.io/badge/minSdk-28-orange.svg)
![Firebase](https://img.shields.io/badge/firebase-enabled-orange.svg)


An Android budget tracking and financial management application built with Kotlin, Firebase, and modern Android architecture components. ZakaZaka helps users take control of their finances through intelligent budget planning, expense tracking, and insightful analytics.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Team Members](#team-members)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Firebase Setup](#firebase-setup)
- [Building and Running](#building-and-running)
- [App Architecture](#app-architecture)
- [Key Activities](#key-activities)
- [Screenshots](#screenshots)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🎯 Overview

**ZakaZaka** is a personal finance management application designed to help users track expenses, manage budgets, and achieve their financial goals. The app provides a comprehensive suite of features including category-based budgeting, transaction tracking with receipt capture, budget goal setting, and detailed analytics.

### Key Highlights

- **Firebase Integration**: Real-time cloud data synchronization and authentication
- **MVVM Architecture**: Clean, maintainable, and testable code structure
- **Category Management**: Organize expenses with categories and subcategories
- **Budget Goals**: Set minimum and maximum spending targets
- **Visual Analytics**: Track spending patterns with detailed reports
- **Receipt Capture**: Attach photos to transactions for record-keeping
- **Multi-Account Support**: Manage multiple bank accounts in one place

---

## 👥 Team Members

This project was developed collaboratively by a dedicated team of developers:

| Team Member | Role |
|------------|------|
| **Nia Diale** | Database / Backend Developer |
| **Zalano Poole** | Database / Backend Developer |
| **Mpho Tlokotsi** | Frontend Developer |
| **Thando Phiri** | Frontend Developer |
| **Ntuthuko (NTK) Senamela** | Project Manager / Quality Assurance & Testing |

---

## ✨ Features

### User Authentication
- **Secure Registration**: Firebase Authentication with email/password
- **User Login**: Secure authentication with session management
- **User Profiles**: Personalized user data stored in Firebase Realtime Database

### Financial Management
- **Account Management**: Create and manage multiple bank accounts
- **Budget Goals**: Set monthly minimum and maximum spending targets
- **Budget Milestones**: Track progress toward financial goals
- **Transaction Tracking**: Record income and expenses with detailed information

### Category Organization
- **Custom Categories**: Create expense categories with budget limits
- **Subcategories**: Further organize expenses within categories
- **Budget Allocation**: Set and track budget limits per category
- **Current Amount Tracking**: Real-time tracking of spending in each category

### Transaction Features
- **Detailed Transactions**: Add amount, date, description, and category
- **Receipt Capture**: Take photos of receipts using device camera
- **Recurring Transactions**: Set up repeating expenses
- **Date Range Filtering**: View transactions by custom date ranges
- **Transaction Details**: View comprehensive information about each transaction

### Analytics & Reports
- **Expense Analytics**: Visual representation of spending patterns
- **Category Breakdown**: See spending distribution across categories
- **Budget vs Actual**: Compare budget limits to actual spending
- **Time-Based Analysis**: Filter and analyze transactions by date range

### User Experience
- **Modern UI**: Clean, intuitive Material Design interface
- **Onboarding Flow**: Guided setup for new users (HowToGetStarted)
- **Bottom Navigation**: Easy access to all major features
- **Real-time Updates**: Instant synchronization across devices

---

## 🛠 Technology Stack

### Core Technologies
- **Language**: Kotlin
- **IDE**: Android Studio
- **UI Framework**: Android SDK (API 28+)
- **Architecture**: MVVM (Model-View-ViewModel)
- **Build System**: Gradle (Kotlin DSL)

### Libraries & Dependencies

#### Android Jetpack
- `androidx.core:core-ktx:1.12.0` - Kotlin extensions
- `androidx.appcompat:appcompat:1.6.1` - Backward compatibility
- `androidx.constraintlayout:constraintlayout:2.1.4` - Layout system
- `androidx.lifecycle:lifecycle-viewmodel-ktx:2.8.4` - ViewModel components
- `androidx.lifecycle:lifecycle-livedata-ktx:2.8.4` - LiveData components
- `androidx.navigation:navigation-fragment-ktx:2.7.7` - Navigation component
- `androidx.recyclerview:recyclerview:1.3.2` - RecyclerView for lists

#### Firebase
- `com.google.firebase:firebase-bom:33.3.0` - Firebase Bill of Materials
- `firebase-auth` - User authentication
- `firebase-database` - Realtime Database
- `firebase-storage` - Cloud Storage (for receipt images)

#### Other Libraries
- `com.google.android.material:material:1.11.0` - Material Design components
- `kotlinx-coroutines-android:1.8.1` - Asynchronous programming

#### Testing
- `junit:4.13.2` - Unit testing
- `androidx.test.ext:junit:1.1.5` - Android testing
- `androidx.test.espresso:espresso-core:3.5.1` - UI testing

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Android Studio**: Arctic Fox (2020.3.1) or later
- **JDK**: Java Development Kit 11 or later
- **Android SDK**: API Level 28 (Android 9.0) or higher
- **Gradle**: 7.0 or later (included with Android Studio)
- **Firebase Account**: For backend services
- **Git**: For version control

### Minimum Device Requirements
- Android 9.0 (API 28) or higher
- 2GB RAM minimum
- Camera permission for receipt capture
- Internet connection for Firebase synchronization

---

## 📦 Installation

### 1. Clone the Repository

```bash
git clone [https://github.com/your-username/zakazaka-budget-app.git](https://github.com/Nia-byte/Personal-Budget-Tracker-App.git)
cd zakazaka-budget-app
```

### 2. Open in Android Studio

1. Launch Android Studio
2. Click "Open an Existing Project"
3. Navigate to the cloned repository folder
4. Wait for Gradle sync to complete

### 3. Configure Firebase

See the [Firebase Setup](#firebase-setup) section below for detailed instructions.

### 4. Build the Project

```bash
./gradlew build
```

Or use Android Studio's Build menu:
- **Build → Make Project** (Ctrl+F9)

---

## 📁 Project Structure

```
zakazaka-budget-app/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/zakazaka/
│   │   │   │   ├── Views/              # Activity classes
│   │   │   │   │   ├── LoginActivity.kt
│   │   │   │   │   ├── CreateAccount.kt
│   │   │   │   │   ├── Dashboard.kt
│   │   │   │   │   ├── HowToGetStarted.kt
│   │   │   │   │   ├── AddAccountActivity.kt
│   │   │   │   │   ├── AccountActivity.kt
│   │   │   │   │   ├── MilestoneActivity.kt
│   │   │   │   │   ├── CreateCategory.kt
│   │   │   │   │   ├── CategoryDetails.kt
│   │   │   │   │   ├── AddTransaction.kt
│   │   │   │   │   ├── ViewAllTransaction.kt
│   │   │   │   │   └── TransactionDetails.kt
│   │   │   │   ├── Adapters/          # RecyclerView adapters
│   │   │   │   │   ├── TransactionAdapter.kt
│   │   │   │   │   └── SubCategoryAdapter.kt
│   │   │   │   ├── Repository/        # Data layer
│   │   │   │   │   ├── UserRepository.kt
│   │   │   │   │   ├── AccountRepository.kt
│   │   │   │   │   ├── CategoryRepository.kt
│   │   │   │   │   ├── SubCategoryRepository.kt
│   │   │   │   │   ├── TransactionRepository.kt
│   │   │   │   │   └── BudgetGoalRepository.kt
│   │   │   │   ├── Models/            # Data models
│   │   │   │   │   ├── UserEntity.kt
│   │   │   │   │   ├── AccountEntity.kt
│   │   │   │   │   ├── CategoryEntity.kt
│   │   │   │   │   ├── SubCategoryEntity.kt
│   │   │   │   │   ├── TransactionEntity.kt
│   │   │   │   │   └── BudgetGoalEntity.kt
│   │   │   │   ├── ViewModels/        # ViewModel classes
│   │   │   │   │   ├── LoginRegistrationViewModel.kt
│   │   │   │   │   ├── AccountViewModel.kt
│   │   │   │   │   ├── CategoryViewModel.kt
│   │   │   │   │   ├── SubCategoryViewModel.kt
│   │   │   │   │   ├── TransactionViewModel.kt
│   │   │   │   │   ├── BudgetGoalViewModel.kt
│   │   │   │   │   ├── HowToViewModel.kt
│   │   │   │   └── └── ViewModelFactory.kt
│   │   │   ├── res/                   # Resources
│   │   │   │   ├── layout/            # XML layouts
│   │   │   │   ├── values/            # Strings, colors, themes
│   │   │   │   ├── drawable/          # Images and icons
│   │   │   │   └── navigation/        # Navigation graphs
│   │   │   └── AndroidManifest.xml    # App manifest
│   │   ├── test/                      # Unit tests
│   │   └── androidTest/               # Instrumentation tests
│   └── build.gradle.kts               # App-level build config
├── gradle/                            # Gradle wrapper
├── build.gradle.kts                   # Project-level build config
├── settings.gradle.kts                # Gradle settings
└── README.md                          # This file
```

---

## 🔥 Firebase Setup

### 1. Create a Firebase Project

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Add Project" or select existing project
3. Follow the setup wizard
4. Enable Google Analytics (optional)

### 2. Register Your Android App

1. In Firebase Console, click "Add App" → Android
2. Enter package name: `com.example.zakazaka`
3. Download `google-services.json`
4. Place the file in `app/` directory

### 3. Enable Firebase Services

#### Authentication
1. Navigate to **Authentication** → **Sign-in method**
2. Enable **Email/Password** authentication

#### Realtime Database
1. Navigate to **Realtime Database**
2. Click "Create Database"
3. Select **Start in test mode** (or production mode with rules)
4. Choose a database location

#### Cloud Storage (for receipt images)
1. Navigate to **Storage**
2. Click "Get Started"
3. Configure security rules:


### 4. Firebase Realtime Database Structure

```
Users/
├── {userId}/
│   ├── userID: String
│   ├── username: String
│   ├── firstName: String
│   ├── lastName: String
│   ├── email: String
│   └── password: String (hashed by Firebase Auth)

Accounts/
├── {userId}/
│   └── {accountId}/
│       ├── accountID: String
│       ├── accountName: String
│       ├── amount: Double
│       ├── type: String
│       ├── bankName: String
│       └── userID: String

Category/
├── {userId}/
│   └── {categoryId}/
│       ├── categoryID: String
│       ├── name: String
│       ├── budgetLimit: Double
│       ├── currentAmount: Double
│       └── userID: String

Sub_Category/
├── {userId}/
│   └── {subCategoryId}/
│       ├── subCategoryID: String
│       ├── name: String
│       ├── description: String
│       ├── budgetLimit: Double
│       ├── currentAmount: Double
│       └── categoryID: String

Transactions/
├── {userId}/
│   └── {transactionId}/
│       ├── transactionID: String
│       ├── date: Long (timestamp)
│       ├── endDate: Long (timestamp)
│       ├── amount: Double
│       ├── repeat: String
│       ├── description: String
│       ├── type: String
│       ├── currency: String
│       ├── subCategoryID: String
│       ├── accountID: String
│       └── imagePath: String (optional)

Budget_Goals/
├── {userId}/
│   └── {budgetGoalId}/
│       ├── budgetGoalID: String
│       ├── minAmount: Double
│       ├── maxAmount: Double
│       ├── month: String
│       ├── status: String
│       └── userID: String
```

---

## 🚀 Building and Running

### Using Android Studio

1. **Run on Emulator**:
   - Open AVD Manager (Tools → AVD Manager)
   - Create/Start an emulator (API 28+)
   - Click Run button (▶️) or press Shift+F10

2. **Run on Physical Device**:
   - Enable Developer Options on your device
   - Enable USB Debugging
   - Connect device via USB
   - Select device from target dropdown
   - Click Run button (▶️)

### Using Command Line

```bash
# Build debug APK
./gradlew assembleDebug

# Install and run debug APK
./gradlew installDebug

# Run tests
./gradlew test

# Run instrumentation tests
./gradlew connectedAndroidTest

# Build release APK (requires signing config)
./gradlew assembleRelease
```

---

## 🏗 App Architecture

### MVVM Pattern

The app follows the **Model-View-ViewModel (MVVM)** architecture pattern:

```
┌─────────────┐
│    View     │ (Activities/Fragments)
│  (Activity) │
└──────┬──────┘
       │ observes
       ↓
┌─────────────┐
│  ViewModel  │ (Business Logic)
│ (LiveData)  │
└──────┬──────┘
       │ uses
       ↓
┌─────────────┐
│ Repository  │ (Data Layer)
│  (Firebase) │
└──────┬──────┘
       │ accesses
       ↓
┌─────────────┐
│   Firebase  │ (Remote Database)
│  (Backend)  │
└─────────────┘
```

### Key Components

#### Views (Activities)
- Handle UI updates and user interactions
- Observe LiveData from ViewModels
- No direct database access

#### ViewModels
- Hold UI-related data
- Survive configuration changes
- Communicate with Repositories
- Provide LiveData to Views

#### Repositories
- Single source of truth for data
- Handle Firebase operations
- Abstract data source from ViewModels
- Use callbacks and LiveData for async operations

#### Firebase Integration
- Real-time data synchronization
- User authentication
- Cloud storage for images
- Scalable backend infrastructure

---

## 📱 Workflows

### Authentication Flow

| Activity | Purpose | Key Features |
|----------|---------|--------------|
| `LoginActivity` | User authentication | Email/password login, navigation to registration |
| `CreateAccount` | New user registration | Form validation, Firebase Auth integration |

### Onboarding Flow

| Activity | Purpose | Key Features |
|----------|---------|--------------|
| `HowToGetStarted` | First-time user setup | Guided checklist for account, category, and budget setup |
| `AddAccountActivity` | Create bank account | Account name, type, bank, initial balance |
| `CreateCategory` | Create expense category | Category name, budget limit |
| `MilestoneActivity` | Set budget goals | Minimum and maximum monthly spending targets |

### Main Dashboard

| Activity | Purpose | Key Features |
|----------|---------|--------------|
| `Dashboard` | Main navigation hub | Bottom navigation, fragment container |
| Fragments: | Home, Categories, Transactions, Analytics, Profile |

### Account Management

| Activity | Purpose | Key Features |
|----------|---------|--------------|
| `AccountActivity` | View all accounts | List of accounts, recent transactions, add new account |

### Category Management

| Activity | Purpose | Key Features |
|----------|---------|--------------|
| `CategoryDetails` | View category details | Budget limits, subcategories, spending analysis by date range |

### Transaction Management

| Activity | Purpose | Key Features |
|----------|---------|--------------|
| `AddTransaction` | Record new transaction | Amount, date, category, subcategory, account, receipt photo |
| `ViewAllTransaction` | View all transactions | Sorted list, date filtering, navigation to details |
| `TransactionDetails` | View transaction details | Full information, receipt image, category hierarchy |

---

## 🎨 Key Features Walkthrough

### 1. User Registration & Login
1. Launch app → `LoginActivity`
2. New users click "Create Account" → `CreateAccount`
3. Enter details and register
4. Login with credentials
5. First-time users directed to `HowToGetStarted`

### 2. Initial Setup (First-Time Users)
1. **Setup Checklist** displays three tasks:
   - Create Bank Account
   - Create Expense Category
   - Set Budget Goal
2. Complete each task in any order
3. Upon completion, navigate to `Dashboard`

### 3. Adding a Transaction
1. Navigate to Transactions tab
2. Click "Add Transaction"
3. Fill in details:
   - Amount
   - Date (date picker)
   - Account (dropdown)
   - Category (dropdown)
   - Subcategory (auto-populated based on category)
   - Description
   - Receipt photo (optional - camera capture)
4. Save transaction
5. Category and subcategory amounts update automatically

### 4. Viewing Transaction History
1. Navigate to Transactions tab
2. View all transactions sorted by date (newest first)
3. Filter by date range:
   - Select start date
   - Select end date
   - Click "Sort" to filter
4. Tap transaction to view full details

### 5. Managing Categories
1. Navigate to Categories tab
2. View all categories with budget limits
3. Tap category to view details:
   - Budget limit
   - Current spending
   - Remaining balance
   - List of subcategories
4. Add subcategories within category details
5. Analyze spending by date range

### 6. Budget Goals
1. Set monthly minimum and maximum spending targets
2. Track progress in analytics
3. Receive status updates (Beginner, Intermediate, Expert)

---

### Authentication
- Login Screen
- Registration Screen

### Onboarding
- How To Get Started Checklist
- Add Account Screen
- Create Category Screen
- Set Budget Goal Screen

### Main Dashboard
- Home Fragment
- Categories Fragment
- Transactions Fragment
- Analytics Fragment
- Profile Fragment

### Transaction Management
- Add Transaction Screen
- Transaction List
- Transaction Details
- Receipt Capture

### Category Management
- Category Details
- Subcategory List
- Spending Analysis

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

### 1. Fork the Repository

```bash
git clone [https://github.com/your-username/zakazaka-budget-app.git](https://github.com/Nia-byte/Personal-Budget-Tracker-App.git)
```

### 2. Create a Feature Branch

```bash
git checkout -b feature/YourFeatureName
```

### 3. Commit Your Changes

```bash
git commit -m "Add: Description of your feature"
```

### 4. Push to Branch

```bash
git push origin feature/YourFeatureName
```

### 5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 ZakaZaka Development Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📞 Contact

### Development Team

- **Nia Diale** - Database/Backend Developer
- **Zalano Poole** - Database/Backend Developer  
- **Mpho Tlokotsi** - Frontend Developer
- **Thando Phiri** - Frontend Developer
- **Ntuthuko (NTK) Senamela** - Project Manager / QA

---

## 🙏 Acknowledgments

- **Firebase** - Backend services and real-time database
- **Android Community** - For excellent libraries and tools
- **Material Design** - UI/UX guidelines
- **Stack Overflow** - Community support and solutions
  - Camera implementation reference (Colocho, S. 2017)
  - ArrayAdapter with Spinner guidance

---

## 📚 Additional Resources

### Documentation
- [Android Developer Guide](https://developer.android.com/guide)
- [Kotlin Documentation](https://kotlinlang.org/docs/home.html)
- [Firebase Documentation](https://firebase.google.com/docs)
- [Material Design](https://material.io/design)
- [MVVM Architecture](https://developer.android.com/topic/architecture)

### Tutorials
- [Android Codelabs](https://codelabs.developers.google.com/?cat=Android)
- [Firebase for Android](https://firebase.google.com/docs/android/setup)
- [Kotlin Coroutines Guide](https://kotlinlang.org/docs/coroutines-guide.html)

---

## 🔄 Version History

- **v1.0.0** (Current) - Initial release
  - User authentication with Firebase
  - Account management
  - Category and subcategory organization
  - Transaction tracking with receipt capture
  - Budget goal setting
  - Date-based filtering and analytics
  - Onboarding flow for new users

