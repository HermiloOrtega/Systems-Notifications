# 🛠 System Admin Panel

## 🧭 Overview
**System Admin Panel** is a centralized monitoring tool developed in **C#**, **SQL Server**, and **Visual Studio** to track and manage application errors across all internally developed systems at AHMSA.

This background application ensures real-time visibility into system behavior by logging all critical exceptions, user actions, and performance anomalies, even if users do not report them manually.

## 💡 Idea & Concept
The panel was built to:
- Detect and store all exceptions triggered by try/catch blocks in production apps
- Provide a UI for reviewing and classifying system bugs
- Allow proactive fixes for issues before they escalate
- Improve developer visibility without relying solely on user reports

## ✨ Features & Functionality
- 📋 Error Logging:
  - Captures: system name, function, module, user, timestamp, exception details
- 🛠 Error Status:
  - Mark errors as New, In Progress, or Resolved
- 🔍 Filtering & Search:
  - By system, error code, module, user, date range
- 📣 Notifications:
  - Windows tray notifications for new or recurring critical issues
- 🖥 Tray Integration:
  - App runs in the system tray, hidden from taskbar
- ⚠️ Singleton Launch:
  - Prevents duplicate instances on the same machine
- 🧪 Session Tracking:
  - Records sign-in/sign-out sessions of all connected systems
  - Adds default duration if session unexpectedly closed
- 🔐 Admin Controls:
  - View logs by severity or module
  - Track unused or underutilized features based on screen usage

## ⚙️ Tech Stack
| Category                | Tools & Frameworks |
|-------------------------|--------------------|
| **Frontend**            | ![WinForms](https://img.shields.io/badge/WinForms-512BD4?logo=.net&logoColor=white&style=for-the-badge) |
| **Backend**             | ![C#](https://img.shields.io/badge/C%23-239120?logo=c-sharp&logoColor=white&style=for-the-badge) |
| **Platform**            | ![Windows App](https://img.shields.io/badge/Windows%20App-0078D4?logo=windows&logoColor=white&style=for-the-badge) |
| **Framework**           | ![.NET Framework](https://img.shields.io/badge/.NET%20Framework-512BD4?logo=.net&logoColor=white&style=for-the-badge) |
| **IDE**                 | ![Visual Studio](https://img.shields.io/badge/Visual%20Studio-5C2D91?logo=visualstudio&logoColor=white&style=for-the-badge) |
| **Security & Identity** | ![Custom Auth](https://img.shields.io/badge/Custom%20Auth-000000?style=for-the-badge&logo=key&logoColor=white) |
| **Database**            | ![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?logo=microsoft-sql-server&logoColor=white&style=for-the-badge) |

## 🏗 Architecture & Design
- Always-on Windows background app
- Queries a shared SQL log table written to by all AHMSA systems (SICAP, SIA, CEA)
- UI dashboard with sortable error log and detail pane
- Screens embedded via modular child-form containers

## 🚀 Installation & Setup
- **Startup:** Auto-starts with Windows boot
- **Deployment:** Developer/admin workstations
- **Database:** Reads from centralized exception log DB

> **Note:** Participating systems must implement the logging interface for full integration.

## 🧑‍💻 My Role & Contributions
- 💼 Architected and implemented the full platform
- 🔧 Designed shared logging schema and Try/Catch interfaces
- 🖥 Built tray system and admin dashboard UI
- 🧠 Developed all real-time background monitoring logic

## 🧗 Challenges & Learnings
- Integrated error reporting across heterogeneous systems
- Handled concurrent log writes and event deduplication
- Improved uptime by identifying frequent fail points
- Learned importance of usage analytics for feature prioritization

## 📈 Future Enhancements
- Email and SMS alert integration
- Historical trend dashboard using Power BI
- GitHub issue tracker or Azure DevOps integration

## 🪪 License
⚠️ **Internal Use Only**  
Originally under MIT License. Changed to **CC BY-NC-ND 4.0** as of April 22, 2025.

## 🔗 Related Projects
- **[SIA](https://github.com/HermiloOrtega/SIA)**
- **[SIA – Petty Cash Module](https://github.com/HermiloOrtega/SIA-Petty-Cash)**
- **[SIA – Material Testing Module](https://github.com/HermiloOrtega/SIA-Material-Testing)**
- **[SICAP](https://github.com/HermiloOrtega/SICAP)**
- **[SICAP Indicators](https://github.com/HermiloOrtega/SICAP-Indicators)**
- **[SICAP Web](https://github.com/HermiloOrtega/SICAP-Web)**
- **[SICAP Updater](https://github.com/HermiloOrtega/SICAP-Web-Updates)**
- **[SICAP Foliador](https://github.com/HermiloOrtega/SICAP-Folio-Manager)**
- **[CEA](https://github.com/HermiloOrtega/CEA)**
- **[CEA Web](https://github.com/HermiloOrtega/CEA-Web)**
- **[CEA Offline](https://github.com/HermiloOrtega/CEA-Offline)**
