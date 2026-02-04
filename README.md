CBOP – Core Banking Operations Portal
---------------------------------------

CBOP (Core Banking Operations Portal) is an enterprise-grade internal banking application designed to simulate real-world core banking operations used by financial institutions.
This project is built for learning, architecture practice, and interview readiness, following industry standards used in large banks and financial organizations.

The system demonstrates:

Secure authentication & authorization

Role-based access control (RBAC)

Maker–Checker workflows

Encrypted sensitive data handling

Oracle database design

Audit logging & reporting

API-driven architecture
----------------------------------------------------------------------
🎯 Objectives

Practice enterprise application architecture

Implement banking-grade security & auditability

Work with ASP.NET Core MVC + Oracle

Understand end-to-end system design (BRD → SDD → Implementation)

Build a portfolio-ready project
-----------------------------------------------------------------
🏗 High-Level Overview

Frontend: ASP.NET Core MVC (Razor, HTML, CSS, JavaScript)

Backend: ASP.NET Core (.NET 8+)

Database: Oracle Database (XE / Local)

Architecture: Layered + Clean separation

Security: Encryption, RBAC, auditing

Reports: PDF & Excel exports
-----------------------------------------------------------------------
🧱 Architecture Pattern

Layered Architecture

Separation of Concerns

Domain-centric design (light DDD)

API-first internal communication

Secure-by-design approach
-----------------------------------------------------------------------
📊 System Diagrams

The following diagrams describe the system visually, as done in enterprise solution documents:

🏗 System Architecture
/docs/diagrams

🔐 Authentication & Authorization Flow
/docs/diagrams

🔁 Maker–Checker Transaction Workflow
/docs/diagrams

📈 Reporting & Export Flow
/docs/diagrams

🗄️ ER Diagram (Oracle Database)
/docs/diagrams

🔄 API Sequence Diagram (Transaction Processing)
/docs/diagrams
---------------------------------------------------------------
🧩 Core Functional Modules
---------------------------------------------------------------
🔐 Authentication & Authorization

Login / Logout

Role-based access control

Policy-based authorization

(Future) Active Directory / SSO integration
---------------------------------------------------------------
👤 User & Role Management

Users

Roles (Admin, Teller, Manager, Auditor)

User–Role mapping
---------------------------------------------------------------
🧑‍💼 Customer Management

Customer onboarding

Encrypted PAN & Aadhaar storage

Customer profile management
---------------------------------------------------------------
🏦 Account Management

Account creation

Balance tracking

Account status control
---------------------------------------------------------------
💸 Transactions

Credit / Debit transactions

Maker–Checker approval flow

Transaction limits & validations

Pending / Approved / Rejected states
---------------------------------------------------------------
📜 Audit & Logging

Complete audit trail

User action tracking

Immutable audit logs
---------------------------------------------------------------
📑 Reporting

Transaction reports

Audit reports

PDF export

Excel export
---------------------------------------------------------------
🔐 Session Management

CBOP implements secure server-side session management to maintain authenticated user context, enforce inactivity timeouts, and protect sensitive banking workflows.
---------------------------------------------------------------
🧩 Session Strategy

Cookie-based authentication (ASP.NET Core Identity)

Server-side session storage

Session used for:

Logged-in user context

Active role and authorization scope

UI-level state (non-sensitive only)
---------------------------------------------------------------
⏱ Session Timeout & Controls
Setting	Value
Idle Timeout	20 minutes
Sliding Expiration	Enabled
Secure Cookie	Enabled
HttpOnly Cookie	Enabled
SameSite Policy	Strict

Sessions automatically expire after inactivity

Re-login required for sensitive operations

Session explicitly cleared on logout
---------------------------------------------------------------
🛡 Security Guidelines

No sensitive data (PAN, Aadhaar, account numbers) stored in session

Sensitive data always fetched securely from database

Session fixation prevented via regeneration on login

Complements Role & Policy-based Authorization
---------------------------------------------------------------
🔄 Future Enhancements

Distributed session store (Redis / SQL)

Concurrent session control

Forced logout on password or role change
---------------------------------------------------------------
🔒 Security Design Highlights

AES encryption for sensitive data

ASP.NET Core Data Protection for key management

Secure password hashing (PBKDF2)

CSRF protection

Input validation

HTTPS enforcement

Principle of least privilege
---------------------------------------------------------------
🗄 Database Design

Oracle Database (XE / Local)

Normalized schema

Foreign key constraints

Indexed transactional tables

Sequence-based primary keys

Encrypted columns for sensitive data
---------------------------------------------------------------
🧪 Testing Strategy

Unit testing (Business logic)

Integration testing (DB + Services)

Role-based access testing

Security & authorization testing

Report validation testing
---------------------------------------------------------------
🚀 Future Enhancements

Active Directory / LDAP integration

Single Sign-On (SSO)

Multi-branch support

Microservices migration

Cloud deployment (Azure / OCI)

Event-driven audit logging
---------------------------------------------------------------
🛠 Technology Stack
Area	Technology
Framework	ASP.NET Core (.NET 10)
UI	Razor, HTML, CSS, JavaScript
ORM	Entity Framework Core
Database	Oracle Database
Auth	ASP.NET Core Identity
Encryption	AES + Data Protection API
Reports	QuestPDF / iText7
Excel	ClosedXML
Logging	Serilog

---

## 📁 Repository Structure (Planned)

<img width="503" height="477" alt="image" src="https://github.com/user-attachments/assets/07d22a2d-4bc3-44f9-b374-bbb8b8f84230" />

---

## 📌 Status

🚧 **In Active Development**  
This project is being built **phase by phase**, following real enterprise delivery practices.

---

## 👨‍💻 Author

**Prafful Chauhan**  
Enterprise Application & Backend Practice Project

---

## 📄 License

This project is for **educational and practice purposes**.
