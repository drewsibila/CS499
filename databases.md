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

* Added SQLite database storage
* Added JDBC database support
* Added a calculation record class
* Added a database class
* Added a service class for database logic
* Added calculation history to the user interface
* Added refresh and clear history options
* Added input validation
* Added prepared statements
* Added error handling
* Added nine new database tests

[Download the Enhanced CS 310 SQLite Calculator](Databases_Enhanced_CS310_SQLite_CLEAN.zip)

## Skills Demonstrated

This enhancement helped me demonstrate skills with:

* Java
* SQLite
* JDBC
* Database design
* Persistent data storage
* SQL
* Prepared statements
* Input validation
* Error handling
* JUnit testing
* Maven
* Tycho
* OSGi

## Code Example

For the database enhancement, I created a SQLite table that stores the expression, result, and date of each calculation.

```java
String sql =
        "CREATE TABLE IF NOT EXISTS calculation_history ("
        + "id INTEGER PRIMARY KEY AUTOINCREMENT, "
        + "expression TEXT NOT NULL, "
        + "result TEXT NOT NULL, "
        + "created_at TEXT NOT NULL"
        + ")";
```

I also used prepared statements when saving calculations.

```java
String sql =
        "INSERT INTO calculation_history "
        + "(expression, result, created_at) "
        + "VALUES (?, ?, ?)";

try (Connection connection = database.getConnection();
        PreparedStatement statement =
                connection.prepareStatement(sql)) {

    statement.setString(1, expression.trim());
    statement.setString(2, result.trim());
    statement.setString(
            3,
            LocalDateTime.now().format(DATE_FORMAT));

    statement.executeUpdate();
}
```

Before saving anything, the service checks that the values are not empty.

```java
private void validateText(
        String value,
        String fieldName) {

    if (value == null || value.trim().isEmpty()) {
        throw new IllegalArgumentException(
                fieldName + " cannot be empty.");
    }
}
```

This shows how the enhanced calculator stores data while also using validation and prepared statements to make the database handling safer.

## What I Learned

The biggest thing I learned was that adding a database involves more than just creating a table.

I had to think about where the database code should go, how the user interface would connect to it, how bad input should be handled, and how the database could be tested.

The biggest challenge was getting the SQLite JDBC driver to work with the older Eclipse and Tycho project setup. The database worked when I tested it manually, but Maven could not find the driver at first.

I fixed the build setup and added the SQLite JAR to the correct bundle configuration. The final Maven build passed all 24 tests with no failures or errors.

## Security

I also improved the security of the project by using prepared statements instead of building SQL commands directly from raw input.

The service checks for empty values and invalid record IDs before sending information to the database.

## Enhancement Narrative

[Read the Full Enhancement Narrative](databases-narrative.md)
