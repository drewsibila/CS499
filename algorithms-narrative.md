# Algorithms and Data Structures Enhancement Narrative

## Artifact Description

The artifact I selected for this enhancement is my CS 320 Project One application. It is a Java program with three main parts: a contact service, a task service, and an appointment service. Each part has its own class, service class, and JUnit tests.

The original project focused on making sure each object followed certain rules. Contacts, tasks, and appointments all had validation requirements, and the service classes allowed records to be added, updated, found, and deleted.

## Why I Selected This Artifact

I selected this project because it already worked, but it still had room for improvement. It was a good project for showing that I can take older code and make it more useful without changing the parts that were already working.

The original version used a HashMap to store contacts, tasks, and appointments by ID. I kept the HashMap because it works well for quickly finding records.

## How I Improved the Artifact

For the enhancement, I added sorting so contacts can be listed by last name and first name, tasks can be listed by name, and appointments can be listed by date.

I also added a PriorityQueue to the appointment service. This makes it easier for the program to find the next appointment based on the earliest date.

I improved validation and error handling for duplicate IDs, missing records, empty IDs, and null values. I also added defensive copying for appointment dates so the date cannot be changed outside of the class without going through the correct methods.

I added more JUnit testing to make sure the new features did not break the original project. The final version had 40 passing tests.

## Course Outcomes

The main course outcome I worked toward was designing and evaluating solutions using algorithms and data structures.

The HashMap is still used for fast lookup by ID. Sorting is used when records need to be shown in a clear order, and the PriorityQueue is used when the program needs to know which appointment comes first.

This helped me understand that one data structure is not always the best choice for every problem.

## Reflection

The biggest thing I learned is that the way data is stored should depend on how the program needs to use it.

The HashMap worked well for finding one record quickly, but it did not automatically sort the records. Adding sorting methods made the program easier to use while still keeping the fast lookup.

The PriorityQueue also helped me understand how programs can organize information by priority.

One of the main challenges was making sure the new features did not break the original features. JUnit testing helped me check every change.

I also had some problems with the Java setup because the original project used Java 8 while some of my testing tools needed Java 17. After fixing the setup and cleaning up duplicate test files, all 40 tests passed.

Overall, this enhancement helped me improve my understanding of data structures, algorithms, testing, validation, and problem solving.
