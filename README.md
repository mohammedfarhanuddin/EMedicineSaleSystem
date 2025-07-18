# E-Medicine Sales System

A Java Swing-based desktop application for managing users, drugs, and sales in a medicine store. This system provides user registration, login, drug inventory management, and order processing, all backed by an Oracle database.

## Features

- **User Registration & Login:**  
  New users can sign up and existing users can log in. User credentials and details are stored in an Oracle database.

- **User Dashboard:**  
  After login, users access a dashboard to:
  - View, insert, update, and delete drug orders.
  - View available drugs.
  - Manage their own orders.

- **Drug Management:**
  - Add new drugs to the inventory.
  - Modify or delete existing drugs.
  - View all available drugs in a tabular format.

- **Order Management:**
  - Place new orders for drugs.
  - Update or delete existing orders.
  - View all order history.

## Project Structure

```
src/
├── emedicine_main.java   # Main entry point: handles sign up and login
├── HomePage.java        # User dashboard: order and drug management
├── UserManage.java      # Admin/user management: CRUD for drugs
├── DrugsAv.java         # View all available drugs
```

## Database

- Uses Oracle Database (JDBC connection).
- Default credentials in code:  
  - Username: `qawi`
  - Password: `qawi`
  - URL: `jdbc:oracle:thin:@localhost:1521:xe`
- Tables referenced: `users`, `drugs`, `history_sales`

## How to Run

1. **Set up Oracle Database**  
   - Create the required tables: `users`, `drugs`, `history_sales`.
   - Update credentials in the source files if needed.

2. **Compile the Java files:**
   ```sh
   javac -d bin src/*.java
   ```

3. **Run the application:**
   ```sh
   java -cp bin emedicine_main
   ```

## Requirements

- Java 8 or higher
- Oracle Database (XE or above)
- Oracle JDBC Driver (ensure it's in your classpath)

## Screenshots

*(Add screenshots of the login, dashboard, and drug management screens here)*

## Notes

- All database credentials are hardcoded for demonstration.  
  For production, use environment variables or configuration files.
- The application uses basic Swing dialogs for UI and error handling.

## License

This project is licensed under the MIT License. The MIT License is a permissive free software license originating at the Massachusetts Institute of Technology (MIT). **Anyone** can use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, regardless of whether they are affiliated with MIT or not.

See the [LICENSE](LICENSE) file for details. 
