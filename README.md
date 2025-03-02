# Warehouse Management System

## Overview
This project is a **Warehouse Management System** implemented in C++. It manages orders, customers, volunteers, and actions related to warehouse operations. The system follows object-oriented principles and is structured for easy expansion and maintenance.

## Features
- Order and Customer management
- Warehouse operations handling
- Volunteer assignment
- Configurable setup through input files

## Project Structure
```
Warehouse_splAssignment-main/
├── bin/              # Compiled binary and object files
├── include/          # Header files defining the project structure
├── src/              # C++ source files containing implementation
├── .vscode/          # VS Code configuration files
├── configFileExample.txt   # Example configuration file
├── Makefile          # Makefile for building the project
└── README.md         # Project documentation
```

## Installation & Build
### Prerequisites
- A C++ compiler (GCC, Clang, or MSVC)
- `make` (for Unix-based systems)

### Steps to Compile
1. Navigate to the project directory:
   ```sh
   cd Warehouse_splAssignment-main
   ```
2. Run the `make` command:
   ```sh
   make
   ```
   This compiles the source files and generates the `warehouse` executable inside the `bin/` directory.

## Running the Application
To run the program, execute:
```sh
./bin/warehouse <configFile>
```
Where `<configFile>` is a configuration file specifying initial warehouse setup.

## Configuration File
The configuration file should be structured as follows:
```
# Example Configuration
<parameter1> <value1>
<parameter2> <value2>
...
```
Refer to `configFileExample.txt` for more details.

## Contributing
Feel free to submit pull requests or report issues. Follow standard C++ coding guidelines and ensure proper documentation of changes.

## License
This project is licensed under an open-source license (if applicable, specify here).

## Author
Developed as part of a **Software Programming Laboratory (SPL) Assignment**.

