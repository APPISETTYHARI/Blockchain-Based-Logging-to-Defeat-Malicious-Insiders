# 🔗 Blockchain-Based Logging to Defeat Malicious Insiders

### The Case of Remote Health Monitoring Systems

> **Major Project** — Bharath Institute of Higher Education and Research, Chennai *(Jan – Apr 2025)*

A blockchain-based security framework with smart contracts and a decentralised audit ledger designed to protect **remote health monitoring systems** against insider threats. The system ensures data integrity, tamper-proof logging, and real-time intrusion detection.

---

## 🎯 Problem Statement

Remote health monitoring systems are vulnerable to **malicious insiders** — authorized users who misuse access to tamper with patient data. Traditional logging mechanisms can be altered or deleted by these insiders, leaving no trace of unauthorized activity.

This project solves that by storing all access logs on a **blockchain-based immutable ledger**, making it impossible to tamper with audit trails.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔐 **Blockchain Audit Logging** | All patient data access is logged with SHA-256 hashing on an immutable ledger |
| 👨‍💼 **Admin Dashboard** | Upload datasets, view all users, monitor patient logs audited by blockchain |
| 👤 **User Portal** | Registration, login, profile management with profile picture upload |
| 🔍 **Hashcode Verification** | Verify patient data integrity by checking blockchain hashcodes |
| 📊 **Disease Analysis** | View disease type results and patient data analytics |
| 🛡️ **Insider Threat Detection** | Detect unauthorized data access patterns through audit trail analysis |
| 📁 **Dataset Management** | Admin can upload and manage healthcare datasets (Excel/CSV) |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | JSP, HTML5, CSS3, JavaScript, jQuery |
| **Backend** | Java Servlets, JSP |
| **Database** | MySQL |
| **Blockchain** | Custom implementation with SHA-256 hashing |
| **Cryptography** | Bouncy Castle (bcprov-jdk15, bouncycastle-jce) |
| **Data Processing** | Apache POI (Excel read/write) |
| **Server** | Apache Tomcat |

---

## 📂 Project Structure

```
├── index.html                    # Landing page
├── adminlogin.jsp                # Admin login portal
├── adminmain.jsp                 # Admin dashboard
├── userlogin.jsp                 # User login portal
├── usermain.jsp                  # User dashboard
├── u_register.jsp                # User registration
├── connect.jsp                   # MySQL database connection
│
├── A_Upload_Datasets*.jsp        # Admin: Upload healthcare datasets
├── A_View_All_Datasets*.jsp      # Admin: View uploaded datasets
├── A_View_All_Users.jsp          # Admin: View registered users
├── A_View_User_Details.jsp       # Admin: Detailed user profiles
├── A_View_All_Patient_Logs_*.jsp # Admin: Blockchain-audited patient logs
│
├── U_Find_Patient_Data_*.jsp     # User: Search patient audit data
├── U_Find_*_By_Hashcode*.jsp     # User: Verify data via blockchain hash
│
├── database/
│   └── database.sql              # Complete MySQL schema & seed data
│
├── css/                          # Stylesheets
├── js/                           # jQuery, Cufon typography, coin-slider
├── images/                       # UI assets and slides
├── Gallery/                      # Gallery images
│
├── WEB-INF/
│   └── lib/                      # Java libraries
│       ├── bcprov-jdk15-138.jar        # Bouncy Castle crypto
│       ├── bouncycastle-jce-*.jar      # JCE provider
│       ├── mysql-connector-java-*.jar  # MySQL JDBC driver
│       ├── poi-3.17.jar                # Apache POI (Excel)
│       ├── servlet-api.jar             # Servlet API
│       ├── mail.jar                    # JavaMail
│       └── ...
│
├── Datasets.xls                  # Sample healthcare dataset
└── Work.txt                      # Project notes
```

---

## 🚀 How to Run

### Prerequisites
- **Java JDK** 8+
- **Apache Tomcat** 8.x or 9.x
- **MySQL** 5.x or 8.x
- **IDE** (Eclipse / IntelliJ with Tomcat plugin)

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/APPISETTYHARI/Blockchain-Based-Logging-to-Defeat-Malicious-Insiders.git
   ```

2. **Import the database**
   ```sql
   mysql -u root -p < database/database.sql
   ```

3. **Configure database connection**
   Open `connect.jsp` and update with your MySQL credentials:
   ```jsp
   String url = "jdbc:mysql://localhost:3306/YOUR_DB_NAME";
   String user = "root";
   String password = "YOUR_PASSWORD";
   ```

4. **Deploy to Tomcat**
   - Import as a **Dynamic Web Project** in Eclipse
   - Or copy the project folder to `tomcat/webapps/`

5. **Access the application**
   - Open `http://localhost:8080/PROJECT_FOLDER/index.html`
   - Admin Login → Manage datasets, view blockchain audit logs
   - User Login → Register, view patient data, verify via hashcode

---

## 🔒 How the Blockchain Logging Works

```
Patient Data Access Request
         ↓
   Generate SHA-256 Hash of Access Record
         ↓
   Store Hash + Metadata on Blockchain Ledger
         ↓
   Link to Previous Block (Chain Integrity)
         ↓
   Immutable Audit Trail Created ✅
```

Any attempt to modify a log entry will break the hash chain, immediately exposing the tampering.

---

## 📜 License

This project is for educational purposes as part of a B.Tech Major Project at Bharath University.

---

<p align="center">Made with ❤️ by <strong><a href="https://linkedin.com/in/appisettyhari">APPISETTY HARI</a></strong></p>
