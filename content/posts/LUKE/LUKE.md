+++
date = '2025-06-20T10:35:33-06:00'
draft = false
title = 'Lipscomb University Kiosk Experience'
+++
![main](/JustinTAlexander-AWebsite/images/LUKEAnnouncement.png)

# Description
The Lipscomb University Kiosk Experience (L.U.K.E.) is a multi-screen kiosk designed to inform and engage. From answering visitor questions to providing fun, interactive experiences, this cutting-edge system showcases the power of technology in enhancing campus navigation and exploration.

L.U.K.E. is built on Processing 4 Java. Work was done to integrate technologies such as Large-Language Model AI. The kiosk was deployed in Lipscomb's Fields Engineering Center in November 2024. 

Github: https://github.com/Lunatic-Labs/Kiosk

# Credits
Developed by the L.U.K.E. team across 3 semesters as part of the course Software Studio. For all semesters, I served as team lead, overseeing iterations 1-5 of the L.U.K.E. software.

On this project, I am credited as:
- Team lead
- Programmer (Python, Java)

# Design
## Class Structure
![classUML](/JustinTAlexander-AWebsite/images/LUKE_ClassStructure_UML.png)
L.U.K.E. was designed as a modification of the observer pattern in which a list of Scenes (observers) is kept up by the class DisplayManager (subject). At the top level, the Processing 4 library is used to receive user input.

## Data Flow
![dataFlowUML](/JustinTAlexander-AWebsite/images/LUKE_DataFlow_UML.png)
L.U.K.E. sought to be as accessible as possible to its owners/maintainers, who were expected to be university officials without Computer Science backgrounds. As such, it was designed to interface directly with the Windows file system.
Information pertaining to many aspects of the kiosk's functionality is formatted into .txt files that are stored alongside the code. This allows the system to be easily updated if a new department or building wishes to house L.U.K.E..

# Postmortem (authored 6/2025)
This past school year, I had my first experiences successfully deploying software projects as a team lead. Today, I offer a retrospective on the Lipscomb University Kiosk Experience, or L.U.K.E..
This kiosk was developed as part of Lipscomb University SoC's Software Studio course, which simulates an Agile software development environment with one-week sprints tracked via Jira and a "client" within the school's faculty.
I spent three semesters as the team lead on L.U.K.E., in which 5 iterations of the software were created.
 
In the first, my team started from full greenfield and went on to design and create the first prototype of the system. L.U.K.E. was created using the Processing 4 software. Our first iteration was completed in Python, but it was later ported to Java to make use of Processing's video libraries. This build was focused on functionality over form, but we were able to create an effective and functional proof of concept.

In our second semester, we expanded on this concept through several rounds of incremental progress, bugfixes, and scripted field tests. We met our goal of deployment in November 2024 when L.U.K.E. Iteration 4 was stationed in the Fields Engineering Center, where he stands today.
Our two graduating team members were replaced by new faces this semester, highlighting the importance of documentation and effective onboarding. 

My last semester with L.U.K.E. was focused entirely on maintenance and documentation, so only myself and one of the junior devs remained on the project. I authored an Owners' Manual in addition to the Programmers' Manual that had been in use by the team. By leveraging the two, we addressed everything related to the kiosk's user-facing operations/maintenance and our team's development processes, respectively.

My experience with L.U.K.E. taught me much about leadership and project management. Our Agile environment utilized frequent standups, both within my team and across the "company". This required technical ability, code literacy, and understanding of project goals, but it also highlighted the importance of "soft skills" such as public speaking and being able to answer tough questions. 

Going through the full development cycle was neither easy nor straightforward, but both my team and our "clients" were happy with the fruits of our labor. I feel that leading the kiosk team allowed me to grow as a leader and developer, as well as giving me the confidence to attempt personal projects.

![logo](JustinTAlexander-AWebsite/images/LUKELogo.jpg)
