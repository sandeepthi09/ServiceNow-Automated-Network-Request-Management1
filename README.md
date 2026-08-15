# Automated Network Request Management in ServiceNow

## 📌 Project Overview

**Automated Network Request Management** is a ServiceNow-based application designed to automate and streamline the process of submitting, processing, approving, fulfilling, and tracking network access requests.

The project provides employees with a standardized **Network Access Request** through the ServiceNow Service Catalog. Instead of depending on manual communication and repeated follow-ups, the solution captures structured request information and uses ServiceNow automation to route the request through its complete lifecycle.

**Team ID:** 23331A4450
**Project:** Automated Network Request Management
**Platform:** ServiceNow
**Project Date:** 10-8-2026

---

## 🎯 Problem Statement

Network-related access requests can become difficult to manage when requests are submitted through informal or inconsistent communication channels.

Common problems include:

* Incomplete request information
* Inconsistent request formats
* Manual data entry
* Repeated communication between employees and the network team
* Delays in approval and fulfillment
* Lack of centralized request tracking
* Difficulty monitoring the current status of a request

The project addresses these challenges by providing a centralized and automated ServiceNow-based request management process.

---

## 💡 Proposed Solution

The solution introduces a **Network Access Request** catalog item in ServiceNow.

The requester provides the required information through a standardized Service Catalog form. ServiceNow then processes the request using configured catalog variables, client-side logic, server-side processing, approval automation, fulfillment tasks, notifications, and status tracking.

### High-Level Workflow

```text
Requester
    ↓
Network Access Request
    ↓
ServiceNow Request / RITM
    ↓
Get Catalog Variables
    ↓
Create Network Request
    ↓
Approval
    ↓
 ┌───────────────┐
 │               │
Approved       Rejected
 │               │
 ↓               ↓
Network Team    Status Update
Task            + Notification
 │
 ↓
Fulfillment
 │
 ↓
Status Update
 │
 ↓
Requester Notification
```

---

## 🚀 Key Features

### 1. Network Access Request

A dedicated Service Catalog item allows users to submit network-related requests using a standardized form.

### 2. Structured Request Information

The request captures important information such as:

* Requested For
* Request Type
* Access Level
* Device Name
* Business Justification
* Requester information
* Other required network details

### 3. Dynamic Form Behaviour

Catalog Client Scripts and UI logic are used to dynamically control and populate request fields based on user input.

### 4. Automated User Information Retrieval

The project uses **GlideAjax** and a server-side **Script Include** to retrieve relevant requester information and populate catalog variables.

### 5. Automated Network Request Creation

Submitted catalog information is retrieved and mapped into the custom **Network Request** record.

### 6. Approval Workflow

Requests can be routed through an approval process before network fulfillment begins.

### 7. Network Team Fulfillment

Approved requests can be converted into fulfillment work for the Network Team through ServiceNow task management.

### 8. Status Tracking

The request lifecycle can be tracked from submission through approval and fulfillment.

### 9. Notifications

Requester notifications provide important updates about the progress and outcome of the request.

### 10. Centralized Management

All network requests are maintained within ServiceNow, providing a centralized location for request management and monitoring.

---

## 🏗️ ServiceNow Architecture

The project follows a layered ServiceNow architecture.

### User Interaction Layer

* Service Catalog
* Network Access Request
* Catalog Variables
* Choice Lists

### Form & Validation Layer

* Catalog Client Scripts
* UI Policies
* Mandatory Fields
* Dynamic Form Behaviour

### Business Logic Layer

* GlideAjax
* Script Includes
* Catalog Variable Retrieval
* Server-side Processing

### Automation Layer

* Flow Designer / Workflow Automation
* Approval
* Record Creation
* Task Creation
* Notifications

### Data Layer

* Request
* Requested Item (RITM)
* Network Request
* Catalog Task

### Fulfillment Layer

* Network Team Assignment
* Task Processing
* Status Updates
* Requester Communication

---

## 🔄 Request Lifecycle

The complete lifecycle of a network request is:

1. Employee opens the Network Access Request.
2. Employee enters the required request details.
3. Catalog Client Script and UI logic process dynamic fields.
4. User information can be retrieved through GlideAjax.
5. Employee submits the request.
6. ServiceNow creates the Request / Requested Item.
7. Catalog variables are retrieved.
8. A Network Request record is created.
9. The request is sent for approval.
10. If rejected, the request follows the rejection path and the requester is informed.
11. If approved, a fulfillment task is assigned to the Network Team.
12. The Network Team processes the request.
13. Request status is updated.
14. The requester receives the relevant notification.
15. The request lifecycle is completed and remains available for tracking.

---

## 🧩 Major ServiceNow Components

| Component                | Purpose                                                |
| ------------------------ | ------------------------------------------------------ |
| Service Catalog          | Provides the Network Access Request form               |
| Catalog Item             | Defines the Network Access Request                     |
| Catalog Variables        | Captures request information                           |
| Catalog Client Script    | Provides dynamic client-side behaviour                 |
| UI Policy                | Controls conditional form behaviour                    |
| GlideAjax                | Communicates between client-side and server-side logic |
| Script Include           | Provides server-side user information processing       |
| Request / RITM           | Maintains the Service Catalog transaction              |
| Network Request Table    | Stores centralized network request information         |
| Flow Designer / Workflow | Automates the request lifecycle                        |
| Approval                 | Controls authorization before fulfillment              |
| Catalog Task             | Provides fulfillment work for the Network Team         |
| Notifications            | Communicates important request updates                 |
| Reports / Lists          | Supports request monitoring and visibility             |

---

## 🗂️ Project Development Phases

The project documentation is organized into separate phases.

```text
1. Ideation Phase
        ↓
2. Requirement Analysis
        ↓
3. Project Design Phase
        ↓
4. Project Planning Phase
        ↓
5. Project Development Phase
        ↓
6. Project Documentation
        ↓
7. Project Demonstration
```

### 1. Ideation Phase

Contains the brainstorming, problem identification, and initial understanding of the project idea and users.

### 2. Requirement Analysis

Contains the technology stack, solution requirements, data flow diagrams, and user stories.

### 3. Project Design Phase

Contains the problem-solution fit, proposed solution, and ServiceNow solution architecture.

### 4. Project Planning Phase

Contains the product backlog, user stories, story points, sprint planning, project tracker, and burndown planning.

### 5. Project Development Phase

Contains User Acceptance Testing, ServiceNow system testing, testcase analysis, defect analysis, performance testing, and development validation.

### 6. Project Documentation

Contains the complete project and ServiceNow implementation documentation.

### 7. Project Demonstration

Contains the final demonstration video and related demonstration material.

---

## 📁 Repository Structure

```text
Servicenow-Automated-Network-Request/
│
├── 1. Ideation Phase/
│   ├── 1.1 Brainstorming Idea.pdf
│   ├── 1.2 Problem Statement.pdf
│   ├── 1.3 Empathy Map Canvas.pdf
│   └── readme.md
│
├── 2. Requirement Analysis/
│   ├── 2.1 Technology Stack.pdf
│   ├── 2.2 Solution Requirements.pdf
│   ├── 2.3 Data Flow Diagrams and User Stories.pdf
│   └── readme.md
│
├── 3. Project Design Phase/
│   ├── 3.1 Solution Fit.pdf
│   ├── 3.2 Proposed Solution.pdf
│   ├── 3.3 Solution Architecture.pdf
│   └── readme.md
│
├── 4. Project Planning Phase/
│   ├── 4.1 Project Planning.pdf
│   └── readme.md
│
├── 5. Project Development Phase/
│   ├── 5.1 User Acceptance Report.pdf
│   ├── 5.2 ServiceNow Testing.pdf
│   └── readme.md
│
├── 6. Project Documentation/
│   ├── 6.1 ServiceNow Capstone Documentation.pdf
│   └── readme.md
│
├── 7. Project Demonstration/
│   ├── Final Project Video.mp4
│   └── readme.md
│
└── README.md
```

---

## 🛠️ Technology & Platform

### Platform

* ServiceNow

### ServiceNow Technologies

* Service Catalog
* Catalog Items
* Catalog Variables
* Catalog Client Scripts
* UI Policies
* GlideAjax
* Script Includes
* Flow Designer / Workflow Automation
* Approvals
* Catalog Tasks
* Notifications
* ServiceNow Tables
* Lists and Reports

---

## 📊 Expected Benefits

The solution is designed to provide:

* Standardized network request submission
* Reduced manual coordination
* Better request-data consistency
* Automated request processing
* Controlled approval
* Faster fulfillment coordination
* Centralized request tracking
* Improved requester visibility
* Better operational management
* A scalable foundation for additional IT service requests

---

## 🔮 Future Enhancements

The solution can be extended with:

* Automated approval routing based on request type
* SLA tracking and escalation
* Performance Analytics dashboards
* Advanced reporting
* Additional network request categories
* More detailed role-based access controls
* Automated fulfillment integrations
* Email and Service Portal enhancements
* Integration with external network management systems
* Predictive or AI-assisted request classification

---

## 👥 Team Information

**Team ID:** 23331A4450

**Project:** Automated Network Request Management

**Platform:** ServiceNow

---

## 📌 Conclusion

The **Automated Network Request Management** project demonstrates how ServiceNow can be used to transform a manual network-request process into a structured, automated, and trackable service workflow.

By combining Service Catalog, client-side configuration, server-side scripting, workflow automation, approvals, fulfillment tasks, notifications, and centralized data management, the solution provides a complete lifecycle for network access requests.

The repository documents the project from **ideation through design, planning, development, documentation, and demonstration**, providing a complete record of the project journey.
