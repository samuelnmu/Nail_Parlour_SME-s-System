# Nail_Parlour_SME-s-System
This is a system that automates Nail_Parlour_SME's
Nail Parlour Management System - Project Documentation

**Project Overview**
This system will provide a comprehensive solution for a nail parlour shop, offering both customer-facing features and administrative tools for the business owner. The system includes online booking, customer loyalty programs, staff scheduling, sales tracking, and marketing capabilities.

**System Features**
1. User (Customer) Features
Service Catalog

View all available services with descriptions and prices

Filter services by category (manicure, pedicure, etc.)

Booking System

Book/unbook services

Select preferred technician (attendee)

View technician availability based on service duration

Pay 10% booking fee via STK push

Automatic time slot blocking when booked

Loyalty Program

Star-based reward system per service category

7 stars = 50% discount on that service

Visual tracking of stars progress

User Account

Booking history

Loyalty status per service

Notification system

2. Admin (Owner) Features
Dashboard

Sales graphs (daily, weekly, monthly)

Customer analytics

Revenue reports

Customer Management

View all clients

Customer segmentation

Marketing email system

Service Management

Add/edit/remove services

Set service durations

Adjust pricing

Staff Management

Technician schedules

Availability management

Performance tracking

Booking Management

View all bookings

Cancel bookings

Handle no-shows (booking fee absorption)


**Technical Architecture**

Frontend
src/
├── components/
│   ├── common/ (buttons, modals, etc.)
│   ├── user/
│   │   ├── ServiceList.jsx
│   │   ├── BookingCalendar.jsx
│   │   ├── TechnicianSelector.jsx
│   │   ├── LoyaltyTracker.jsx
│   │   └── PaymentModal.jsx
│   └── admin/
│       ├── Dashboard.jsx
│       ├── CustomerManager.jsx
│       ├── ServiceEditor.jsx
│       └── Reports.jsx
├── pages/
│   ├── UserHome.jsx
│   ├── AdminHome.jsx
│   ├── Login.jsx
│   └── Signup.jsx
├── services/ (API calls)
├── context/ (React context)
├── hooks/ (custom hooks)
├── utils/ (helper functions)
└── styles/ (CSS/SASS)

Backend
src/
├── controllers/
│   ├── authController.js
│   ├── bookingController.js
│   ├── serviceController.js
│   ├── userController.js
│   ├── adminController.js
│   └── paymentController.js
├── models/
│   ├── User.js
│   ├── Service.js
│   ├── Booking.js
│   ├── Technician.js
│   └── Loyalty.js
├── routes/
│   ├── authRoutes.js
│   ├── bookingRoutes.js
│   ├── serviceRoutes.js
│   ├── userRoutes.js
│   └── adminRoutes.js
├── middleware/ (auth, validation)
├── services/ (business logic)
├── utils/ (helpers)
└── config/ (database, env)

**Payment Integration (STK Push)**
For M-Pesa STK push integration in Kenya:

Register for Daraja API at Safaricom Developer Portal

Implement the following flow:

Frontend collects phone number

Backend initiates STK push via /mpesa/stkpush/v1/processrequest

Handle callback with payment confirmation

Update booking status upon successful payment

**Additional Robust Features**
Automated Reminders

SMS/email reminders 24 hours before appointment

Follow-up messages after service

Inventory Management

Track nail polish and other product inventory

Low stock alerts

Technician Performance Metrics

Most popular technician

Average service time vs estimated

Customer satisfaction ratings

Dynamic Pricing

Peak/off-peak pricing

Package deals for multiple services

Mobile App Integration

Push notifications

Mobile booking convenience

Virtual Try-On

AR feature to preview nail designs

**Implementation Roadmap**
Phase 1 (5 days)

Core booking system

Basic admin dashboard

User authentication

Phase 2 (4 days)

Loyalty program implementation

Payment integration

Technician scheduling

Phase 3 (3 weeks)

Advanced reporting

Marketing tools

Refinements and testing

Phase 4 (4 days)

Additional features (inventory, etc.)

Performance optimization

Deployment

**Technology Stack**
Frontend: React, Redux, Material-UI/SASS, Chart.js

Backend: Node.js, Express, MongoDB/Mongoose

Payment: M-Pesa Daraja API

Email: SendGrid/Mailchimp API

Hosting: AWS/Heroku (backend), Netlify/Vercel (frontend)

CI/CD: GitHub Actions