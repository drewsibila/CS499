# Databases Enhancement Narrative

## Artifact Description

The artifact I selected is a Java calculator project from CS 310. The original calculator could complete basic math problems, but it did not save any calculation history.

For this enhancement, I added a SQLite database so the calculator can save, load, and manage past calculations.

## Why I Selected This Artifact

I selected this project because it gave me a good way to show my database skills in a working program.

Instead of making a completely separate database project, I added the database directly to the calculator. The calculator now saves completed calculations and shows them in a history panel. The history is still there after the program is closed and opened again.

## How I Improved the Artifact

I added classes for the calculation record, database connection, and service logic.

I also updated the user interface so the user can view, refresh, and clear the calculation history.

The database can save records, return them in newest-first order, count records, delete records, and clear the full history.

I also improved the project by adding input validation, error handling, prepared statements, and JUnit testing.

I created nine new tests for the database features. These tests checked saving, loading, counting, sorting, deleting, clearing, and rejecting invalid input.

The final Maven build showed 24 tests passed with no failures or errors.

## Course Outcomes

This enhancement helped me meet the course outcome involving the use of tools and techniques to build useful computing solutions.

I used Java, JDBC, SQLite, Maven, Tycho, and JUnit to improve an existing program.

I also separated the database code, service code, record object, and user interface so the project would be easier to understand and maintain.

The project also helped me make progress with security. I used prepared statements instead of building SQL commands directly from raw input. I also checked for empty values and invalid record IDs before sending data to the database.

## Reflection

The biggest thing I learned is that adding a database takes more than just creating a table.

I had to think about where the database code should go, how the user interface would use it, how to handle bad input, and how to test the database without affecting real data.

The biggest challenge was getting the SQLite JDBC driver to work with the older Eclipse and Tycho setup. The database worked when I ran it manually, but Maven could not find the driver at first.

I also had to work through problems with Java 17, Java 8, Maven, Tycho, OSGi, and the Eclipse target platform.

After fixing the build setup and adding the SQLite JAR to the correct bundle configuration, the final build passed all 24 tests.

Overall, this enhancement helped me improve my database, testing, software design, security, and troubleshooting skills.
