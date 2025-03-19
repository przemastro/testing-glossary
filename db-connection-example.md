# SQL Database Connection Examples

This document contains examples of how to connect to an SQL database and retrieve data from a hypothetical `users` table with the following columns: `id`, `name`, and `email`. The examples use different programming languages.

---

## Python (using `pyodbc`)

```python
import pyodbc

# Connection settings
server = 'localhost'
database = 'TestDB'
username = 'your_username'
password = 'your_password'

# Create connection
conn = pyodbc.connect(f'DRIVER={{SQL Server}};SERVER={server};DATABASE={database};UID={username};PWD={password}')
cursor = conn.cursor()

# SQL Query
cursor.execute("SELECT id, name, email FROM users")

# Fetch data
rows = cursor.fetchall()

# Print results
for row in rows:
    print(f"ID: {row.id}, Name: {row.name}, Email: {row.email}")

# Close connection
conn.close()

```

## Java - Connecting to SQL Database and Fetching Data

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.Statement;

public class DatabaseExample {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/TestDB";
        String username = "your_username";
        String password = "your_password";

        try (Connection connection = DriverManager.getConnection(url, username, password);
             Statement statement = connection.createStatement()) {

            String query = "SELECT id, name, email FROM users";
            ResultSet resultSet = statement.executeQuery(query);

            while (resultSet.next()) {
                int id = resultSet.getInt("id");
                String name = resultSet.getString("name");
                String email = resultSet.getString("email");
                System.out.println("ID: " + id + ", Name: " + name + ", Email: " + email);
            }

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}


```
## Kotlin - Connecting to SQL Database and Fetching Data

```kotlin
import java.sql.Connection
import java.sql.DriverManager
import java.sql.ResultSet
import java.sql.Statement

fun main() {
    val url = "jdbc:mysql://localhost:3306/TestDB"
    val username = "your_username"
    val password = "your_password"

    try {
        DriverManager.getConnection(url, username, password).use { connection ->
            val statement: Statement = connection.createStatement()
            val query = "SELECT id, name, email FROM users"
            val resultSet: ResultSet = statement.executeQuery(query)

            while (resultSet.next()) {
                val id = resultSet.getInt("id")
                val name = resultSet.getString("name")
                val email = resultSet.getString("email")
                println("ID: $id, Name: $name, Email: $email")
            }
        }
    } catch (e: Exception) {
        e.printStackTrace()
    }
}

```
## JavaScript - Connecting to SQL Database and Fetching Data

```javascript
const mysql = require('mysql');

const connection = mysql.createConnection({
  host: 'localhost',
  user: 'your_username',
  password: 'your_password',
  database: 'TestDB'
});

connection.connect((err) => {
  if (err) {
    console.error('Error connecting to the database: ' + err.stack);
    return;
  }
  console.log('Connected to the database as id ' + connection.threadId);

  const query = 'SELECT id, name, email FROM users';
  connection.query(query, (err, results) => {
    if (err) {
      console.error('Error executing query: ' + err.stack);
      return;
    }

    results.forEach((row) => {
      console.log(`ID: ${row.id}, Name: ${row.name}, Email: ${row.email}`);
    });
  });

  connection.end();
});


```
## TypeScript - Connecting to SQL Database and Fetching Data

```typescript
import mysql from 'mysql';

const connection = mysql.createConnection({
  host: 'localhost',
  user: 'your_username',
  password: 'your_password',
  database: 'TestDB'
});

connection.connect((err) => {
  if (err) {
    console.error('Error connecting to the database: ' + err.stack);
    return;
  }
  console.log('Connected to the database as id ' + connection.threadId);

  const query = 'SELECT id, name, email FROM users';
  connection.query(query, (err, results) => {
    if (err) {
      console.error('Error executing query: ' + err.stack);
      return;
    }

    results.forEach((row: any) => {
      console.log(`ID: ${row.id}, Name: ${row.name}, Email: ${row.email}`);
    });
  });

  connection.end();
});
