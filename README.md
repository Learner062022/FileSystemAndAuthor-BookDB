# FileSystemAndAuthor-BookDB

This repository contains SQL scripts to create and manage a simple database for a file system and an author-book relationship. The script includes commands to create tables, insert records, and execute various queries to retrieve data from these tables.

## Purpose
This project provides a structured way to manage and query a hierarchical file system and a many-to-many relationship between authors and books. It is useful for anyone looking to understand or implement database design and querying techniques for these common scenarios.

## Tables

### Folders

Stores information about folders.

- **Columns:**
  - **`ID`**: Unique identifier for each folder.
  - **`name`**: Name of the folder.
  - **`created_date`**: Date when the folder was created.
  - **`accessed_date`**: Date when the folder was last accessed.
  - **`modified_date`**: Date when the folder was last modified.

### Files

Stores information about files.

- **Columns:**
  - **`ID`**: Unique identifier for each file.
  - **`folder_ID`**: Identifier of the folder the file belongs to.
  - **`name`**: Name of the file.
  - **`created_date`**: Date when the file was created.
  - **`accessed_date`**: Date when the file was last accessed.
  - **`modified_date`**: Date when the file was last modified.
  - **`file_size_bytes`**: Size of the file in bytes.

### Authors

Stores information about authors.

- **Columns:**
  - **`ID`**: Unique identifier for each author.
  - **`first_name`**: First name of the author.
  - **`last_name`**: Last name of the author.

### Books

Stores information about books.

- **Columns:**
  - **`ID`**: Unique identifier for each book.
  - **`title`**: Title of the book.

### Author_Book

Join table for authors and books.

- **Columns:**
  - **`author_ID`**: Identifier of the author.
  - **`book_ID`**: Identifier of the book.

## Queries

### File System Queries

1. Display all the names of all the files in a given folder.
2. Display the folder name and file names for files in a given folder.
3. Display the folder name and file names for files in a given folder if they haven’t been accessed this year.
4. Display all folders and what files they contain, even if they contain none.
5. Display all folders and what files they contain, even if they contain none. Sort by file size.
6. Display all the files and what folders they are in.
7. Display all the files and what folders they are in. Sort alphabetically by folder name and then file size.
8. Display all files and what folders they are in that were created in the last seven days.
9. Display the name of a given folder and the total size of the files in that folder.
10. Display the names of all the folders and all the files.
11. Display the names, date created, and date last accessed for all the folders and all the files.

### Author-Book Queries

1. List all the authors and the books they’ve written.

## Usage

To use the script, follow these steps:

## Usage

To use the script, follow these steps:

### Using MySQL:

1. **Clone the repository:**
    ```sh
    git clone https://github.com/Learner062022/FileSystemAndAuthorBookDB.git
    ```
2. Navigate to the repository directory:
    ```sh
    cd FileSystemAndAuthorBookDB
    ```
3. Execute the SQL script:
    ```sh
    mysql -u <username> -p <database_name> < WorkingWithMultipleTables
    ```

### Using MySQL Online Editor:

1. Open the MySQL Online Editor.
2. Copy and paste the content of the `WorkingWithMultipleTables` file into the editor.
3. Execute the script.
   
# Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure that your code adheres to the established style and conventions, and that you include appropriate tests.

# License
This project is licensed under the [GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.txt).

For detailed information and the complete SQL script, refer to the **'WorkingWithMultipleTables'** file in the repository.
