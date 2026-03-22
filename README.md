# Capstone_Project_2

## Group Members
* Nguyen Xuan Hieu 
* Hoang Viet Hung 
* Nguyen The Hung
* Tran Xuan Tien
* Vu Van Thien
* Nguyen Van Quoc Tuan

## What is Medivault Smart Clinic?
Medivault Smart Clinic is a fully self-hostable, open-source medical clinic management system designed for doctors and medical practices who want complete control over their patient data and clinic operations. 
Built with modern web technologies, it provides a comprehensive solution for managing patients, prescriptions, appointments, and medical records.

## Features

### Doctor Portal
**Dashboard Analytics**
* Patient statistics and growth trends
* Recent activity overview
* Quick access to pending tasks
* Visual charts and graphs

**Patient Management**
* Complete patient registry
* Detailed medical histories
* Patient search and filtering
* Add/edit/delete patient records
* Track patient visits and outcomes

**Prescription System**
* Rich text prescription editor
* Support for Arabic and English text
* PDF generation with custom branding
* Prescription templates
* Print and download prescriptions
* Prescription history tracking

**Assistant Management**
* Invite and manage clinic assistants
* Assign roles and permissions
* Monitor assistant activity

---

### Assistant Portal
**Patient Operations**
* View assigned patient list
* Update patient contact information
* Schedule and manage appointments
* Add patient notes and updates

**Daily Operations**
* Appointment calendar
* Patient check-in/check-out
* Task management

---

### Authentication & User Management
**User Registration**
* Email-based registration
* Role selection (Doctor/Assistant)
* Email verification (if configured)

**Login Options**
* Standard email/password login
* Google OAuth integration (optional)
* "Remember me" functionality

**Profile Management**
* Update personal information
* Change password
* Manage clinic details 

**Password Recovery**
* Email-based password reset
* Secure token generation

---

### Progressive Web App (PWA)
* **Install on Mobile:** Add to home screen on iOS/Android
* **Offline Capability:** Basic functionality works offline
* **Responsive Design:** Works on desktop, tablet, and mobile
* **App-like Experience:** Native app feel on mobile devices

### PDF Generation
* **Professional Prescriptions:** Generate branded PDF prescriptions
* **WeasyPrint Integration:** High-quality PDF rendering
* **Custom Templates:** Customize prescription layout
* **Print Ready:** Optimized for A4 printing

---

### Core Workflows

#### For Doctors:
1. Log in to Doctor Portal (/doctor/)
2. View Dashboard (Check appointments, review stats)
3. Manage Patients (/doctor/patients/)
4. Create Prescriptions (/doctor/prescriptions/)
5. Manage Staff (/doctor/assistants/)

#### For Assistants:
1. Log in to Assistant Portal (/assistant/)
2. View Today's Schedule (Check-ins, appointments)
3. Manage Patients (/assistant/patients/)
4. Support Doctor (Prepare files, admin tasks)

---

## Technology Stack
* **Backend:** Django 4.2+ (Python web framework)
* **Database:** PostgreSQL 12+ (production) or SQLite (development)
* **Frontend:** TailwindCSS 3.0+, Alpine.js
* **PDF Generation:** WeasyPrint (HTML to PDF)
* **Authentication:** Django Auth + Google OAuth
* **PWA:** Service Workers, Web Manifest
* **Deployment:** Docker, Docker Compose, Gunicorn

---

## Database Schema
**Key Models:**
* **User (Django built-in):** Authentication
* **Profile (accounts):** User profiles, clinic info
* **Patient (doctor):** Patient records
* **MedicalHistory (doctor):** Patient medical histories
* **Prescription (doctor):** Prescriptions
* **Appointment (doctor):** Appointments

## Project Structure
```text
├── accounts/                   # User authentication & profiles
│   ├── models.py               # User, Profile models
│   ├── views.py                # Login, register, profile views
│   ├── forms.py                # User forms
│   └── templates/accounts/     # Auth templates
│
├── doctor/                     # Doctor portal
│   ├── models.py               # Patient, Prescription models
│   ├── views.py                # Doctor dashboard, patient management
│   ├── forms.py                # Patient, prescription forms
│   ├── urls.py                 # Doctor routes
│   └── templates/doctor/       # Doctor templates
│
├── assistant/                  # Assistant portal
│   ├── views.py                # Assistant dashboard
│   ├── urls.py                 # Assistant routes
│   └── templates/assistant/    # Assistant templates
│
├── static/                     # Static files
│   ├── css/                    # Stylesheets
│   ├── js/                     # JavaScript files
│   ├── images/                 # Images and logos
│   ├── manifest.json           # PWA manifest
│   └── serviceworker.js        # PWA service worker
│
├── templates/                  # Base templates
│   ├── base.html               # Base layout
│   ├── landing.html            # Landing page
│   └── components/             # Reusable components
│
├── media/                      # User uploads
│   ├── profile_pics/           # Profile pictures
│   └── prescriptions/          # Generated PDFs
│
├── imhotep_smart_clinic/       # Project settings
│   ├── settings.py             # Django settings
│   ├── urls.py                 # URL configuration
│   └── wsgi.py                 # WSGI config
│
├── docker-compose.yml          # Docker configuration
├── Dockerfile                  # Docker image definition
├── requirements.txt            # Python dependencies
├── .env.example                # Environment template
├── manage.py                   # Django management script
└── README.md                   # This file
```

