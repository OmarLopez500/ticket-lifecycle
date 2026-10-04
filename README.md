osTicket - Help Desk Ticket Lifecycle

<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

Project Overview

This project demonstrates a realistic IT help desk ticket lifecycle using the open-source ticketing platform osTicket.

For this scenario, John Cena from the Marketing department reports that he is unable to access the company's Marketing shared drive. The project demonstrates how a help desk technician receives the request, reviews and assigns the ticket, performs troubleshooting, identifies the root cause, communicates with the user, and documents the final resolution.

The goal of this project is to demonstrate practical help desk skills such as:

Ticket documentation

User communication

Network troubleshooting

Access and permissions troubleshooting

Root cause analysis

Resolution documentation

Ticket closure

Lab Environment

The following technologies were used for this project:

Microsoft Azure - Virtual machine environment

Remote Desktop (RDP) - Remote access to the Windows virtual machine

Internet Information Services (IIS) - Web server environment

osTicket - Help desk ticketing platform

Windows 10 (21H2) - Operating system

Ticket Scenario

👤 User

John Cena
Department: Marketing

🎫 Issue

John reports that he can no longer access the Marketing shared drive.

He receives the following type of message when attempting to access:

\\fileserver\Marketing

Windows cannot access \fileserver\Marketing. You do not have permission to access this network resource.

John states that he was able to access the folder the previous day and needs the files for an active Marketing project.

Ticket Lifecycle

The ticket is handled through four primary stages:

Ticket Creation

Review and Assignment

Troubleshooting

Resolution and Closure

1. Ticket Creation

The first step is documenting John's request in osTicket.

The technician records the affected user, department, reported symptoms, and the resource the user is attempting to access.

<p>
  <img width="1762" height="977" alt="Ticket Creation" src="https://github.com/user-attachments/assets/121df3ca-d294-453f-9152-9297dbdd3fc0" />
</p>

Ticket Information

Requester: John Cena
Department: Marketing
Issue: Unable to access Marketing shared drive
Resource: \\fileserver\Marketing
Priority: Normal

The purpose of this stage is to create a clear record of the problem before troubleshooting begins.

2. Review and Assignment

After the ticket is created, the technician reviews the request and assigns it appropriately.

<p>
  <img width="1297" height="955" alt="Ticket Review and Assignment" src="https://github.com/user-attachments/assets/2d786d2f-666a-48af-9e6b-cb715fa4a4b0" />
</p>

The technician confirms that the issue involves access to a network resource rather than a general computer or Internet problem.

The ticket is kept organized so the technician can track ownership, priority, communication, and progress.

3. Troubleshooting

The technician begins investigating the problem and communicates with John to gather additional information.

<p>
  <img width="1198" height="661" alt="Troubleshooting" src="https://github.com/user-attachments/assets/7c37722b-369a-4581-bde1-f30ea04a1213" />
</p>

Troubleshooting Steps

1. Test another network share

John is asked to access:

\\fileserver\Public

The Public share works successfully.

2. Verify connectivity to the file server

The technician has John test the server:

ping fileserver

The server responds, indicating that network connectivity is working.

3. Narrow down the problem

Because John can reach the file server and access another shared folder, the problem appears to be isolated to the Marketing share.

4. Check account permissions

The technician reviews John's account permissions and discovers that his account is no longer a member of the required Marketing security group.

Root Cause

John's account lost membership in the security group that provides access to the Marketing shared drive.

4. Resolution and Closure

The technician restores John's membership in the appropriate Marketing security group.

<p>
  <img width="1198" height="661" alt="Resolution and Closure" src="https://github.com/user-attachments/assets/26d5f1d4-2699-4537-9d56-f877139f05f9" />
</p>

John is instructed to sign out of Windows and sign back in so the updated permissions can be applied.

He then tests:

\\fileserver\Marketing

The Marketing folder opens successfully.

Resolution

Restored John's membership in the Marketing security group. User signed back into Windows and successfully accessed the Marketing shared drive.

Ticket Status: Resolved

Technician Notes

Problem

John Cena from Marketing was unable to access the Marketing shared drive.

Investigation

Verified the user could access other network shares.

Confirmed connectivity to the file server.

Determined the issue was isolated to the Marketing share.

Reviewed the user's account permissions.

Found that the user was missing from the Marketing security group.

Root Cause

The user's account no longer had membership in the security group required to access the Marketing shared drive.

Solution

Restored the user's Marketing security group membership and had the user sign out and sign back in.

Verification

John successfully opened:

\\fileserver\Marketing

and confirmed that the required files were accessible.

What I Learned

This project demonstrates that help desk troubleshooting is more than simply fixing a technical problem. A technician must also properly document the issue, communicate with the user, investigate the symptoms, identify the root cause, and record the resolution.

The main skills demonstrated in this project include:

Creating and documenting support tickets

Reviewing and assigning tickets

Communicating with end users

Troubleshooting network connectivity

Troubleshooting shared-folder access

Understanding user permissions and security groups

Identifying root causes

Documenting technical resolutions

Closing tickets after verifying the solution

Ticket Workflow

┌──────────────────┐
│  Ticket Created  │
└────────┬─────────┘
         │
         ▼
┌──────────────────────┐
│ Review & Assignment  │
└────────┬─────────────┘
         │
         ▼
┌──────────────────┐
│   Troubleshoot   │
└────────┬─────────┘
         │
         ▼
┌──────────────────────┐
│ Identify Root Cause  │
└────────┬─────────────┘
         │
         ▼
┌──────────────────┐
│ Apply Resolution │
└────────┬─────────┘
         │
         ▼
┌──────────────────────┐
│ Verify With User     │
└────────┬─────────────┘
         │
         ▼
┌──────────────────┐
│ Ticket Resolved  │
└──────────────────┘

Summary

This osTicket project demonstrates a complete help desk workflow using a realistic user-access scenario.

John Cena reports an access problem → Ticket is created → Technician reviews the issue → Network connectivity is tested → Permissions are investigated → Root cause is identified → Access is restored → User verifies the fix → Ticket is resolved.

This workflow demonstrates how an IT support technician can use a ticketing system to organize, troubleshoot, document, and resolve a real-world support request.
