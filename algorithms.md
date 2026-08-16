# Algorithms and Data Structures

## Artifact Overview

For this enhancement, I used my CS 320 Project One application.

The project is a Java application with three main parts: a contact service, a task service, and an appointment service. Each section includes its own class, service class, and JUnit tests.

## Original Artifact

The original version used a HashMap to store contacts, tasks, and appointments by ID. This worked well for quickly finding individual records.

[Download the Original CS 320 Artifact](03_Algorithms_Original_CS320.zip)

## Enhanced Artifact

For the enhancement, I kept the HashMap because it was still a good choice for fast lookup, but I added new ways to organize and work with the data.

Some of the main improvements included:

- Added sorting for contacts by last name and first name
- Added sorting for tasks by name
- Added sorting for appointments by date
- Added a PriorityQueue for appointments
- Improved validation
- Improved duplicate ID handling
- Improved error handling for missing records
- Added defensive copying for appointment dates
- Expanded JUnit testing

[Download the Enhanced CS 320 Artifact](04_Algorithms_Enhanced_CS320.zip)

## Skills Demonstrated

This enhancement helped me demonstrate skills with:

- Java
- HashMap
- PriorityQueue
- Sorting
- Comparators
- Data structures
- Algorithms
- Validation
- Error handling
- JUnit testing
- Java collections

## What I Learned

The biggest thing I learned was that the way data is stored should depend on how the program needs to use it.

The HashMap still worked well for quickly finding a record by ID, but it did not automatically organize the records. Adding sorting made the information easier to use without removing the fast lookup.

The PriorityQueue also helped me understand how a program can organize items by priority. In this project, the earliest appointment has the highest priority.

Another challenge was making sure the new features did not break the original project. I used JUnit testing throughout the enhancement, and the final project had 40 passing tests.

## Enhancement Narrative

[Read the Full Enhancement Narrative](algorithms-narrative.md)
