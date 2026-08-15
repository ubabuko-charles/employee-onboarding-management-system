# employee-onboarding-management-system
# Employee Onboarding Management System

A business application built with **Microsoft Power Apps, Power Automate, SharePoint, and Microsoft 365/Outlook** to manage employee onboarding from employee registration through task completion and document verification.

The system provides a centralized way for HR to manage employees, assign onboarding tasks, track progress, manage onboarding documents, and automate notifications throughout the onboarding process.

## Overview

Employee onboarding can involve multiple employees, tasks, documents, emails, and manual follow-ups. This application brings these activities into one solution and uses Power Automate to automate key parts of the onboarding process.

## Technologies Used

* Microsoft Power Apps
* Microsoft Power Automate
* SharePoint Online
* Microsoft Outlook / Microsoft 365

## Key Features

### Employee Management

* Add and manage employee records
* Store employee information including employee ID, department, job title, manager, email, and start date
* Search employees by name
* View detailed employee information
* Validate required employee information before submission

### Onboarding Task Management

* Create onboarding tasks for employees
* Assign tasks to responsible users
* Set task due dates
* Track task status
* Update tasks through:

  * Not Started
  * In Progress
  * Completed
* View tasks associated with individual employees
* Filter onboarding tasks by employee, status, and assigned user

### Document Management

* Track employee onboarding documents
* Record document type and notes
* Track document status through:

  * Pending
  * Submitted
  * Verified

### Dashboard

The application provides summary information for onboarding activities, including:

* Total Employees
* Not Started
* In Progress
* Completed

This gives HR a quick overview of onboarding progress.

## Power Automate Workflows

### 1. New Employee Welcome Email

When a new employee is added to the SharePoint Employees list, Power Automate automatically sends a personalized welcome email to the employee containing their name and start date.

**SharePoint → Power Automate → Outlook**

### 2. Onboarding Task Notification

When HR creates a new onboarding task, Power Automate automatically sends an email to the person responsible for the task.

The notification includes:

* Employee
* Task
* Due Date

**SharePoint → Power Automate → Outlook**

### 3. Onboarding Completion Notification

When an employee's onboarding status becomes **Completed**, Power Automate sends a completion email to the employee.

**SharePoint → Power Automate → Outlook**

### 4. Automatic Onboarding Status

The system evaluates an employee's onboarding tasks and automatically updates the employee's onboarding status.

When all tasks are completed:

**Onboarding Status → Completed**

When outstanding tasks remain:

**Onboarding Status → In Progress**

This allows the system to automatically reflect the employee's actual onboarding progress.

## Application Structure

The solution is built around three main SharePoint data sources:

### Employees

Stores employee information and overall onboarding status.

### Onboarding Tasks

Stores tasks assigned to employees, including task status, responsible users, due dates, and notes.

### Documents

Stores onboarding document information, document status, and notes.

Power Apps provides the user interface while SharePoint stores the application data and Power Automate handles business process automation and email notifications.

## Business Process

The overall onboarding process works as follows:

```text
Employee Added
      ↓
Welcome Email Sent
      ↓
HR Creates Onboarding Tasks
      ↓
Task Assignment Email Sent
      ↓
Tasks Completed
      ↓
Onboarding Progress Updated Automatically
      ↓
All Tasks Completed
      ↓
Employee Status → Completed
      ↓
Completion Email Sent
```

## Validation and User Experience

The application includes validation to prevent incomplete employee records from being submitted.

Required information includes:

* Employee Name
* Email
* Employee ID
* Department
* Start Date

The application also provides search, status tracking, dashboard summaries, and structured screens for managing employees, tasks, and documents.

## Testing

The application was tested end-to-end across its main functionality, including:

* Employee creation and validation
* Employee search
* Employee details
* Task creation
* Task status updates
* Document management
* Dashboard information
* Welcome email automation
* Task notification automation
* Onboarding completion notification
* Automatic onboarding status updates

All planned functional tests were completed successfully.

## What I Learned

This project provided practical experience with:

* Building business applications with Power Apps
* Working with SharePoint as a data source
* Creating automated business workflows with Power Automate
* Connecting Power Apps, SharePoint, and Outlook
* Working with related business records
* Implementing validation and filtering
* Automating business logic based on record status
* Designing applications around real-world business processes

## Project Outcome

The completed solution demonstrates how Microsoft Power Platform can be used to create a connected business application that combines **data management, user interfaces, workflow automation, notifications, and business process logic** in one solution.
