# Hospital Patient Management System

## Overview

The Hospital Patient Management System is a web application designed to manage patient records efficiently. It allows users to add new patients, search for existing patients, and download patient records in CSV format. The application is built using Flask for the backend and HTML/CSS/JavaScript for the frontend.

## Features

- **Add New Patient**: Users can add new patient records by providing the patient's name, age, and problems.
- **Search Patient**: Users can search for a patient by their ID to view detailed information.
- **Download Patient Records**: Users can download the entire patient database as a CSV file.

## Setup Instructions

### Prerequisites

- Python 3.x
- Flask
- Pandas
- A web browser

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/prashantshirk/doc-entery.git
   cd doc-entery
   ```

2. **Install Dependencies**:
   Ensure you have `pip` installed, then run:
   ```bash
   pip install flask pandas
   ```

3. **Run the Application**:
   Start the Flask server by executing:
   ```bash
   python app.py
   ```
   The application will be accessible at `http://127.0.0.1:5000`.

### File Structure

- `app.py`: The main Flask application file handling routes and logic.
- `index.html`: The frontend HTML file for the user interface.
- `patients.csv`: The CSV file storing patient data.

## API Endpoints

- **`GET /`**: Renders the homepage of the application. Response: HTML page.
- **`POST /add_patient`**: Adds a new patient to the database. Request Body: JSON object containing `name`, `age`, and `problems`. Response: JSON object indicating success or failure.
- **`GET /get_patient/<int:patient_id>`**: Retrieves information for a specific patient by ID. Response: JSON object with patient details or an error message.
- **`GET /download_csv`**: Downloads the patient records as a CSV file. Response: CSV file download.

## Usage

1. **Add a New Patient**: Navigate to the "Add New Patient" section. Fill in the patient's name, age, and problems. Click "Add Patient" to save the record.
2. **Search for a Patient**: Navigate to the "Search Patient" section. Enter the patient ID and click "Search" to view details.
3. **Download Patient Records**: Click the "Download Patient Records" button to download the CSV file.

## Troubleshooting

- **Server Errors**: Check the console output for error messages.
- **CSV File Issues**: Ensure the `patients.csv` file is not open in another program when running the application.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License.








# List of books

books = ["Python Basics", "C Programming", "Data Structures"]

# Dictionary to store availability

status = {"Python Basics": "Available",

"C Programming": "Available",

"Data Structures": "Available"}#Stack for last issued books

issued stack = []

#Queue for issue requests

issue_queue=[

#Function to display all books

def display_books():

for b in books:

print(b, "->", status[b])

# Issue book

def issue_book():

name = input("Enter book name to issue: ")

if name in books and status[name] == "Available":

status[name] = "Issued"

issued_stack.append(name)

print(name, "Issued Successfully")

else:

print("Book not available")

# Return book

def return_book():

name = input("Enter book name to return: ")

if name in books and status[name] == "Issued":

status [name] = "Available"

print(name, "Returned Successfully")

else:

print("Invalid Return")

# View last issued book

def view_last_issued():if issued stack:

print("Last Issued:", issued_stack[-1])

else:

print("No books issued yet")

# Add to issue queue

def add_issue_request():

req = input("Enter book name to request: ")

issue_queue.append(req)

print(req, "Added to issue queue")

# View issue queue

def view_issue_queue():

print("Issue Requests:", issue_queue)

# Menu

while True:

print("\n1.Display Books 2.Issue Book 3.Return Book 4.Last Issued")

print("5.Add Issue Request 6.View Issue Queue 7.Exit")

ch = int(input("Enter Choice: "))

if ch ==1

display_books()

elif ch ==2

issue_book()

elif ch ==3

return_book()

elif ch ==4,

view_last_issued

elif ch == 5:

add_issue_request()

elif ch ==6

view_issue_queue()elif ch== 7:

break

else:

print("Invalid Choice")
