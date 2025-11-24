# cReddit: Automated Testing Suite

This repository is for all the E2E testing Scripts for the Reddit clone website and mobile app [cReddit](https://creddit.tech/)

   

A comprehensive automated testing framework designed for **cReddit**, a full-stack clone of Reddit. This repository contains end-to-end (E2E) test scripts for both the **Web Application** (using Selenium WebDriver) and the **Mobile Application** (using Appium), ensuring robust regression testing across platforms.

-----

## 🚀 Test Coverage

The framework covers critical user journeys and functional requirements, including but not limited to:

### 🌐 Web Automation (Selenium)

  * **Authentication**: Sign Up, Login, Google OAuth integration, Password Recovery.
  * **Community Management**: Creating subreddits, joining/leaving communities, and moderation tools.
  * **Content Creation**: Posting text, images, and links; commenting; and upvoting/downvoting.
  * **User Profile**: Editing profile settings, avatar uploads, and privacy configurations.
  * **Real-Time Features**: Chat functionality and notifications.
  * **Search & Navigation**: Global search functionality and sidebar navigation.

### 📱 Mobile Automation (Appium)

  * **Device Interaction**: Touch gestures, scrolling, and mobile-specific UI validation.
  * **Account Management**: Login flows and profile updates.
  * **Moderation Actions**: Approving/removing posts and user management.
  * **Settings**: modifying account preferences (Email, Password).

-----

## 🛠️ Tech Stack

  * **Language**: Python 3.x
  * **Web Automation**: Selenium WebDriver
  * **Mobile Automation**: Appium Client
  * **Browsers Supported**: Chrome, Firefox (GeckoDriver)
  * **Architecture**: Page Object Model (POM) inspired structure for maintainability.

-----

## 📂 Project Structure

The repository is organized by platform and feature module to ensure scalability.

```
├── Mobile_Tests/           # Appium Scripts for Android/iOS
│   ├── Comments/           # Comment interaction tests
│   ├── Moderation/         # Mod tools (User, Content, General)
│   ├── Profile/            # Profile view and edit tests
│   ├── Registration/       # Auth flow tests
│   ├── Settings/           # Account settings tests
│   ├── main_mobile_test.py # Test runner for mobile suite
│   └── ...
├── Web_tests/              # Selenium Scripts for Web
│   ├── Community/          # Subreddit creation and management
│   ├── Registration/       # Login, Signup, Logout logic
│   ├── Settings/           # User preferences tests
│   ├── main_web_test.py    # Test runner for web suite
│   └── ...
├── Web_Text_Files/         # Test data and logging outputs
└── requirements.txt        # Python dependencies
```

-----

## 🔧 Installation & Usage

### Prerequisites

  * Python 3.8+ installed.
  * **Google Chrome** and matching **ChromeDriver**.
  * **Appium Server** running (for mobile tests).
  * An Android Emulator or Real Device connected via ADB.

### 1\. Setup Environment

```bash
# Clone the repository
git clone https://github.com/AbdullahAyman02/cReddit-Testing.git
cd cReddit-Testing

# Install dependencies
pip install selenium Appium-Python-Client
```

### 2\. Run Web Tests

To execute the full regression suite for the web application:

```bash
python Web_tests/main_web_test.py
```

*Note: Ensure `chrome.py` or `firefox.py` is configured with the correct driver path.*

### 3\. Run Mobile Tests

Start your Appium server and ensure an emulator is running. Then execute:

```bash
python Mobile_Tests/main_mobile_test.py
```

-----

## 🧠 Key Highlights

  * **Modular Design**: Tests are broken down into functional areas (e.g., `Community`, `Registration`), making debugging and maintenance significantly easier compared to monolithic scripts.
  * **Cross-Browser Support**: Includes configuration for both **Chrome** and **Firefox**, demonstrating understanding of browser compatibility testing.
  * **Robust Error Handling**: Scripts include explicit waits and error logging to handle dynamic DOM elements and network latency.

-----

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.
