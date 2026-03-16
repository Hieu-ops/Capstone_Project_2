# Capstone_Project_2
What is Imhotep Smart Clinic?
Imhotep Smart Clinic is a fully self-hostable, open-source medical clinic management system designed for doctors and medical practices who want complete control over their patient data and clinic operations. 
Built with modern web technologies, it provides a comprehensive solution for managing patients, prescriptions, appointments, and medical records.

Features
Doctor Portal
Dashboard Analytics

Patient statistics and growth trends
Recent activity overview
Quick access to pending tasks
Visual charts and graphs

Patient Management 
Complete patient registry
Detailed medical histories
Patient search and filtering
Add/edit/delete patient records
Track patient visits and outcomes

Prescription System 
Rich text prescription editor
Support for Arabic and English text
PDF generation with custom branding
Prescription templates
Print and download prescriptions
Prescription history tracking

Assistant Management 
Invite and manage clinic assistants
Assign roles and permissions
Monitor assistant activity

Assistant Portal
Patient Operations
View assigned patient list
Update patient contact information
Schedule and manage appointments
Add patient notes and updates
Daily Operations
Appointment calendar
Patient check-in/check-out
Task management

Authentication & User Management
Located at: 
User Registration 
Email-based registration
Role selection (Doctor/Assistant)
Email verification (if configured)

Login Options 
Standard email/password login
Google OAuth integration (optional)
"Remember me" functionality
Profile Management 

Update personal information
Change password
Manage clinic details 
Password Recovery 
Email-based password reset
Secure token generation

Progressive Web App (PWA)
Install on Mobile: Add to home screen on iOS/Android
Offline Capability: Basic functionality works offline
Responsive Design: Works on desktop, tablet, and mobile
App-like Experience: Native app feel on mobile devices
Multilingual Support
Arabic Support: Full RTL support for Arabic prescriptions
English Interface: Default English UI
Easy Translation: i18n ready for additional languages
PDF Generation
Professional Prescriptions: Generate branded PDF prescriptions
WeasyPrint Integration: High-quality PDF rendering
Custom Templates: Customize prescription layout
Print Ready: Optimized for A4 printing

Usage Guide
First-Time Setup
Access the Application

Navigate to http://localhost:8000
You'll see the landing page
Create Your Account

Click "Register" 
Choose role: "Doctor" for clinic owner
Fill in your details
Verify email if configured
Complete Your Profile

Log in and go to Profile 
Add clinic information
Upload profile picture
Set your specialization
Add Your First Patient

Go to Doctor Portal → Patients 
Click "Add New Patient"
Fill in patient details
Save the record
Create a Prescription

Select a patient
Click "New Prescription" 
Use the rich text editor for prescription details
Add medications, dosages, instructions
Save and generate PDF

Technology Stack
Backend: Django 4.2+ (Python web framework)
Database: PostgreSQL 12+ (production) or SQLite (development)
Frontend: TailwindCSS 3.0+, Alpine.js
PDF Generation: WeasyPrint (HTML to PDF)
Authentication: Django Auth + Google OAuth
PWA: Service Workers, Web Manifest
Deployment: Docker, Docker Compose, Gunicorn

Database Schema
Key Models:

User (Django built-in): Authentication
Profile (accounts): User profiles, clinic info
Patient (doctor): Patient records
MedicalHistory (doctor): Patient medical histories
Prescription (doctor): Prescriptions
Appointment (doctor): Appointments

1. Log in to Doctor Portal (/doctor/)
   ↓
2. View Dashboard
   - Check today's appointments
   - Review patient statistics
   ↓
3. Manage Patients (/doctor/patients/)
   - Add new patients
   - Update medical histories
   - Review past visits
   ↓
4. Create Prescriptions (/doctor/prescriptions/)
   - Select patient
   - Write prescription
   - Generate PDF
   - Print or email to patient
   ↓
5. Manage Staff (/doctor/assistants/)
   - Invite assistants
   - Assign permissions

1. Log in to Assistant Portal (/assistant/)
   ↓
2. View Today's Schedule
   - Check appointments
   - Patient check-ins
   ↓
3. Manage Patients (/assistant/patients/)
   - Update contact info
   - Schedule appointments
   - Add notes
   ↓
4. Support Doctor
   - Prepare patient files
   - Handle administrative tasks
