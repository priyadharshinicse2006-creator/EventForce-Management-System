🎪 EventForce Management System

Salesforce CRM Implementation for Event Management

"Salesforce" (https://img.shields.io/badge/Salesforce-CRM-00A1E0?style=for-the-badge&logo=salesforce&logoColor=white)
"Apex" (https://img.shields.io/badge/Apex-Development-1798C1?style=for-the-badge)
"Flows" (https://img.shields.io/badge/Salesforce-Flows-00A1E0?style=for-the-badge)
"CRM" (https://img.shields.io/badge/Domain-CRM-blue?style=for-the-badge)

📌 Project Overview

EventForce Management System is a Salesforce-based CRM solution designed to streamline event management operations.

The system provides a centralized platform for managing events, clients, vendors, venues, and feedback. It also automates important business processes such as event reminders, cancellation approvals, venue availability updates, and double-booking prevention.

The project demonstrates practical implementation of Salesforce configuration, automation, Apex development, security, reporting, and dashboards.

---

🎯 Objectives

- Centralize event management operations
- Manage client bookings and event details
- Coordinate vendors and event services
- Manage venue reservations and availability
- Automate event reminders and approval workflows
- Prevent venue double bookings
- Collect and manage client feedback
- Provide reports and dashboards for business insights
- Implement role-based access and data security

---

🛠️ Technologies & Salesforce Features

Technology / Feature| Usage
Salesforce CRM| Core platform
Lightning App| User interface
Custom Objects| Data management
Apex| Business logic
Apex Triggers| Event automation
Salesforce Flows| Process automation
SOQL| Data querying
Validation Rules| Data validation
Formula Fields| Automated calculations
Approval Process| Cancellation workflow
Reports & Dashboards| Business analytics
Profiles & Roles| User access
Permission Sets| Additional permissions
Sharing Rules| Record-level security

---

🗂️ Custom Objects

The application contains the following custom objects:

- Event
- Client
- Vendor
- Venue
- Feedback
- Event Vendor – Junction Object

The Event Vendor junction object establishes a many-to-many relationship between Events and Vendors.

---

🔗 Data Relationships

Client
   │
   └── Lookup ──> Event <── Lookup ── Venue
                    │
                    │
                    └── Event Vendor
                           │
                           └── Vendor

Client
   │
   └── Lookup ──> Feedback <── Lookup ── Event

Relationship Types

- Event → Client: Lookup
- Event → Venue: Lookup
- Feedback → Event: Lookup
- Feedback → Client: Lookup
- Event Vendor → Event: Master-Detail
- Event Vendor → Vendor: Master-Detail

---

⚡ Key Features

📅 Event Management

- Create and manage events
- Track event dates and status
- Support multiple event types
- Calculate event budgets using Formula Fields
- Manage event cancellation requests

👤 Client Management

- Store client information
- Manage email and phone details
- Maintain address and location information
- Validate client email addresses

🤝 Vendor Management

- Manage vendor details
- Track vendor service types
- Manage vendor availability
- Support services such as catering, decoration, photography, videography, lighting, and transportation

🏢 Venue Management

- Store venue details
- Track venue capacity
- Monitor venue availability
- Automatically update venue status

⭐ Feedback Management

- Collect client feedback
- Store ratings from 1–5
- Maintain detailed comments

---

🤖 Automation

1. Client Event Reminder

A Salesforce Record-Triggered Flow sends an automated reminder email to the client 3 days before a confirmed event.

2. Event Cancellation Approval

An Approval Process manages event cancellation requests and sends email notifications during the approval workflow.

3. Venue Availability Automation

An Apex Class and Trigger automatically updates venue availability based on the event status.

- Confirmed Event → Venue Reserved
- Cancelled Event → Venue Available

4. Double Booking Prevention

An Apex Trigger prevents multiple events from being scheduled at the same venue on the same date.

5. Scheduled Event Completion

Batch Apex + Scheduled Apex automatically identifies past events and updates their status to Completed.

---

📊 Reports & Dashboards

The project includes Salesforce reporting and analytics features such as:

📈 Reports

- Upcoming Events by Month
- Event Budget Summary
- Event Schedule Analysis
- Vendor Performance Insights

📊 Dashboard

EventForce Operations Dashboard

Provides a visual overview of upcoming events and operational metrics.

---

🔐 Security & Access Control

The application uses Salesforce security features to control data access:

- Profiles
- Roles
- Permission Sets
- Organization-Wide Defaults (OWD)
- Sharing Rules
- Role Hierarchy

👥 User Roles

Role| Responsibility
Event Admin| Overall system administration
Event Coordinator| Event and client management
Vendor Manager| Vendor and service management
Client| Event access and feedback

The project configures different permissions for these user roles to control access to Events, Clients, Vendors, Venues, and Feedback.

---

🔄 Project Workflow

Client
   ↓
Event Booking
   ↓
Event Coordinator
   ↓
Venue + Vendor Assignment
   ↓
Event Confirmation
   ↓
Automated Client Reminder
   ↓
Event Execution
   ↓
Feedback Collection
   ↓
Reports & Dashboard

For cancellation:

Cancellation Request
        ↓
Approval Process
        ↓
Manager Review
     ↙     ↘
 Approved   Rejected
    ↓          ↓
Canceled    Rejected
    ↓
Email Notification

---

📱 Salesforce Lightning App

A custom Event Planner Lightning App was created to provide centralized access to:

- Events
- Clients
- Vendors
- Venues
- Feedback
- Reports
- Dashboards

---

💡 Business Value

The EventForce Management System is designed to:

- Reduce manual event management activities
- Improve booking efficiency
- Provide centralized customer information
- Automate repetitive business processes
- Improve communication through automated notifications
- Provide real-time operational visibility
- Support data-driven decision making

The project specification identifies goals including reducing manual processes and improving booking efficiency through Salesforce automation and centralized CRM data.

---

📚 Learning Outcomes

Through this project, I gained practical experience in:

- Salesforce CRM
- Salesforce Lightning
- Custom Objects and Fields
- Lookup Relationships
- Master-Detail Relationships
- Many-to-Many Relationships
- Salesforce Flows
- Apex Classes
- Apex Triggers
- Batch Apex
- Scheduled Apex
- Approval Processes
- Validation Rules
- Formula Fields
- Reports and Dashboards
- Profiles and Roles
- Permission Sets
- Sharing Rules
- Salesforce Security

---

👩‍💻 Project Domain

CRM | Salesforce | Event Management | Cloud Application

---

🚀 Project Status

Completed – Salesforce Implementation

The project covers the major stages of implementation including requirement analysis, backend configuration, automation, UI customization, reporting, data migration, testing, and security configuration.

---

📌 Future Enhancements

Potential future improvements could include:

- Enhanced Lightning UI components
- Advanced event analytics
- Additional automated notifications
- More detailed vendor performance tracking
- Extended reporting and dashboard capabilities

---

⭐ If you find this project useful, consider giving the repository a star!
