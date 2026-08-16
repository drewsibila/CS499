# Databases

## Artifact Overview

For this enhancement, I used my Java calculator project from CS 310.

The original calculator could perform basic math operations, but it did not save any calculation history after the program was closed.

## Original Artifact

The original version focused on the calculator functions and did not include permanent data storage.

[Download the Original CS 310 Calculator](05_Databases_Original_CS310.zip)

## Enhanced Artifact

For the enhancement, I added a SQLite database so the calculator can save and manage calculation history.

Some of the main improvements included:

- Added SQLite database storage
- Added JDBC database support
- Added a calculation record class
- Added a database class
- Added a service class for database logic
- Added calculation history to the user interface
- Added refresh and clear history options
- Added input validation
- Added prepared statements
- Added error handling
- Added nine new database tests

[Download the Enhanced CS 310 SQLite Calculator](Databases_Enhanced_CS310_SQLite_CLEAN.zip)

## Skills Demonstrated

This enhancement helped me demonstrate skills with:

- Java
- SQLite
- JDBC
- Database design
- Persistent data storage
- SQL
- Prepared statements
- Input validation
- Error handling
- JUnit testing
- Maven
- Tycho
- OSGi

## What I Learned

The biggest thing I learned was that adding a database involves more than just creating a table.

I had to think about where the database code should go, how the user interface would connect to it, how bad input should be handled, and how the database could be tested.

The biggest challenge was getting the SQLite JDBC driver to work with the older Eclipse and Tycho project setup. The database worked when I tested it manually, but Maven could not find the driver at first.

I fixed the build setup and added the SQLite JAR to the correct bundle configuration. The final Maven build passed all 24 tests with no failures or errors.

## Security

I also improved the security of the project by using prepared statements instead of building SQL commands directly from raw input.

The service checks for empty values and invalid record IDs before sending information to the database.

## Enhancement Narrative

The full narrative for this enhancement explains why I selected the artifact, what I changed, what I learned, and how the enhancement connects to the CS 499 course outcomes.
