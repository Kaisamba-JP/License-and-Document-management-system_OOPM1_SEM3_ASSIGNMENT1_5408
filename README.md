# READ ME

# License and Document Management System (LADMS)

## About the project

LADMS is a Python console program built with Object-Oriented Programming. It solves a real government problem: keeping track of citizens and the official documents and licenses issued to them. It belongs to the Government domain, as a Digital Permit and License Management System.

A citizen registers and receives an automatically generated citizen ID (for example CDS-0001). The citizen can then register documents, and each document gets its own reference number. The documents supported are the National ID, Birth Certificate, Death Certificate, Driver's License, Passport, Voter ID Card and NASSIT Card.

## Features

- Register a new citizen with a full name, date of birth, phone number, address and password
- Citizen ID, document reference numbers and age generated automatically
- Register documents, with the fields matched to each document type
- Public list of citizen names only
- Full citizen details shown in a table, but only with the admin password
- A citizen's documents shown only with their own ID and password
- Input checks and clear messages, such as "Wrong password, please try again or enter 0 to go back to the start."
- Duplicate documents blocked: a citizen cannot register the same document type twice

## How it meets Digital Public Goods (DPG) standards

- **Open-source:** the full source code is public on GitHub, and anyone can read, run and improve it.
- **Inclusive and accessible:** it uses simple text menus and plain-language prompts. It needs no internet, no installation beyond Python, and no special hardware. Every screen lets the user enter 0 to go back, and every wrong input gets a helpful message.
- **Privacy-respecting:** data is stored in memory only, and nothing is written to a file or sent anywhere. Passwords are never stored as plain text, because only a SHA-256 hash is kept. The public view shows names only, details need the admin password, and documents need the citizen's own ID and password.
- **Modular and reusable:** the code is split into separate files, and each class can be reused in another project.

## OOP concepts used

| Concept | Place being used |
|---|---|
| Classes, attributes and objects | Citizen, Document and LicenseDocumentSystem |
| Data structure: list | self.citizens in system.py, and self.documents in citizen.py |
| Tuples | document_types and field_labels in document.py |
| Instance methods | get_age, check_password, has_document, add_document |
| Class methods | generate_citizen_id, generate_reference_number |
| Static methods | hash_password, calculate_age, find_type |
| Inheritance and polymorphism | Seven document classes extend Document and override display_info |
| Encapsulation | Private __password_hash |

## Project structure

- **main.py:** starts the program
- **system.py:** menu, input and validation, and the list of citizens
- **citizen.py:** the Citizen class
- **document.py:** the Document parent class and its seven child classes

## How to run

1. Install Python 3.8 or newer. No extra libraries are needed.
2. Download all four .py files into the same folder.
3. Open a terminal in that folder and run: `python main.py`

## Example usage

Welcome screen and main menu, Registering a new citizen (option 1):


Registering a document, with a wrong password and an unavailable document name (option 2):


Viewing citizens: names for everyone, full table with the admin password (option 3):


Viewing a citizen's documents with their ID and password (option 4):


Wrong input handling:


## Author

**Author's name:** Ibrahim JP Kai-samba

**Student ID:** 905005408