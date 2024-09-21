# 📚 Library Management System using Python & MySQL By Mohammad Waris

---


## 🚀 Introduction:

This intermediate project is a user-friendly **Library Management System** that helps manage books with various functionalities, including:
- 📖 Add books with details
- ❌ Delete books from the list
- 👀 View the list of available books
- 📤 Issue books to students or others
- 📥 Return books with status updates

This system provides an intuitive interface for library operations and efficiently tracks issued and returned books using **Python** and **MySQL**.

---

## ⚙️ Dependencies:

To run this project, the following dependencies are required:
- `tkinter` for the GUI
- `pillow` for image processing
- `pymysql` for MySQL integration

You can install them using the following commands:
```bash
pip install tk
pip install pillow
pip install pymysql
```

_**Note**: Ensure that you have `tkinter` (for the GUI) and `pillow` (for PIL) properly installed as they are essential to run the project._

---

## ❗ Important Steps: Setting up MySQL

1. **MySQL Installation**:  
   - Ensure you have installed MySQL for your operating system. If not, follow this [video guide](https://www.youtube.com/watch?v=N3B3OonC2AU&t=343s) (not sponsored).
   - It's recommended to use the password as `root` for easier setup.

2. **Database Setup**:  
   After installing MySQL and setting up your environment:
   - Open the **MySQL Command Line Client** (search for it using the Windows key if you're on Windows).
   - Enter the password (default: `root`).
   
   Now, run the following commands to set up the necessary database and tables:

   ```sql
   -- Create a new database
   create database db;

   -- Switch to the new database
   use db;

   -- Create a table for books
   create table books(
       bid varchar(20) primary key, 
       title varchar(30), 
       author varchar(30), 
       status varchar(30)
   );

   -- Create a table for issued books
   create table books_issued(
       bid varchar(20) primary key, 
       issuedto varchar(30)
   );
   ```

3. **Verify the Setup**:
   - To check if your tables were created successfully, use the command:
     ```sql
     show tables;
     ```
   - To view the content of your `books` table:
     ```sql
     select * from books;
     ```

   Similarly, you can view issued books using:
   ```sql
   select * from books_issued;
   ```

---

## 💻 How to Run the Project:

1. **Run the Program**:  
   To launch the system, simply run the `main.py` file:
   ```bash
   python main.py
   ```

2. **Using the System**:  
   After running the program, a user interface (UI) will pop up. You can now perform various actions:
   - **Add a Book**: After entering book details, verify in MySQL using:
     ```sql
     select * from books;
     ```
   - **Delete a Book**: After deleting, confirm the removal using the same `select` command.
   - **Issue a Book**: To check the issued book status:
     ```sql
     select * from books_issued;
     ```
   - **Return a Book**: The status will update from "Issued" to "Available" in the `books` table.

   Congratulations! If you've followed all the steps correctly, your library system should be fully functional.

---

## 📜 Conclusion

The **Library Management System** is an ideal project for anyone looking to explore Python’s integration with MySQL. It offers an interactive, easy-to-use interface to manage books and track their status. By using this system, you’ll develop a solid understanding of database operations and GUI design using Python.

