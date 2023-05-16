The Library Management System (LMS) is a Python-based program designed to manage the operations of a library. It provides functionalities such as displaying books, issuing books to members, returning books, adding new books to the library, importing books from an external source, and saving data to files.

The project consists of the following main components:

Class Definition: The LMS class serves as the core of the program. It takes four parameters during initialization: list_of_books, members_file, transactions_file, and library_name. These parameters define the file paths for storing book data, member data, transaction data, and the name of the library, respectively. The class also contains various methods for different operations.

Initialization: Upon creating an instance of the LMS class, the constructor initializes the object's attributes. It loads existing book data, member data, and transaction data from the respective files into dictionaries and lists for further processing. It also sets the next_transaction_id based on the highest transaction ID in the loaded transactions, ensuring unique transaction IDs for new transactions.

Displaying Books: The display_books method prints a formatted list of all books in the library. It retrieves the book details from the books_dict dictionary and presents them in a tabular format.

Issuing Books: The issue_books method allows a librarian to issue a book to a member. It prompts for the book ID and member ID, verifies their validity, and updates the book's status and lender details accordingly. It also creates a new transaction record with the issue date and optional rent fee.

Returning Books: The return_books method handles the return of a book. It prompts for the book ID, checks if the book is issued, updates the book's status, and sets the return date in the corresponding transaction record.

Adding Books: The add_books method enables the addition of new books to the library. It prompts for book details such as ID, title, lender name, lend date, and status. The entered data is then added to the books_dict dictionary.

Saving Data: The save_data method is responsible for persisting the current state of books, members, and transactions to their respective files. It iterates over the dictionaries and lists, writing the data in a comma-separated format.

Importing Books: The import_books method facilitates the import of books from an external source using a web API. It prompts for the number of books to import and the title of the books to search for. It sends a request to the API, retrieves the book data, and adds it to the books_dict dictionary.

Quitting Program: The quit_program method is called when the user chooses to exit the program. It invokes the save_data method to save the data and displays a goodbye message.

Running the Program: The run method is the main entry point for the program. It presents a menu to the user and repeatedly prompts for input until the user chooses to quit. Based on the user's choice, it calls the corresponding methods to perform the desired operation.

Main Program: The main program creates an instance of the LMS class, passing the necessary file paths and library name. It then calls the run method to start the program's execution.
