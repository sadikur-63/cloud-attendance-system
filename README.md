# Cloud-Based Attendance System

A simple cloud-based student attendance system built for a Cloud Computing project.

## Project Overview

This system allows a teacher to mark a student's attendance through a web dashboard. The attendance information is processed using AWS cloud services and stored in a cloud database.

When a student is marked **Absent**, the system automatically sends an email notification.

## Architecture

Dashboard → API Gateway → Lambda → DynamoDB

When absent:

Lambda → Amazon SES → Student Email

## Technologies Used

- HTML
- CSS
- JavaScript
- GitHub Pages
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon SES

## AWS Services

### Amazon API Gateway
Receives attendance requests from the web dashboard and forwards them to AWS Lambda.

### AWS Lambda
Processes the attendance request, checks student information, stores attendance data, and triggers an email alert when necessary.

### Amazon DynamoDB
Stores student information and attendance records.

Tables:
- `AttendanceStudents`
- `AttendanceRecords`

### Amazon SES
Sends automatic email notifications when a student is marked absent.

## Attendance Flow

1. Teacher opens the dashboard.
2. Teacher enters/selects student information.
3. Teacher selects Present or Absent.
4. Dashboard sends the attendance request to API Gateway.
5. API Gateway invokes Lambda.
6. Lambda validates the student.
7. Lambda stores the attendance record in DynamoDB.
8. If the status is Absent, Lambda sends an email through Amazon SES.
9. The student receives the attendance notification.

## Dashboard

The project dashboard is hosted using GitHub Pages.

## Project Purpose

The purpose of this project is to demonstrate how cloud computing and serverless AWS services can be used to build an attendance management system with automatic email notifications.

## Future Improvements

Possible future improvements include:

- Multiple student accounts
- Teacher login
- Attendance reports
- Attendance statistics
- AI-based attendance analysis
- Exporting attendance reports
- Mobile-friendly improvements

## Project Team

Cloud Computing Project  
Dongshin University
