# UiPath Basic Framework

![image](https://github.com/AnkRaw/UiPath-Basic-Framework/assets/45765236/2e5abcd5-4287-49c4-befe-f133e4a028ec)


## Introduction

The Basic Framework is a UiPath Framework designed to simplify automation processes by providing a robust structure that includes automatic error logging and seamless continuation after errors. This framework is user-friendly, making it accessible for users with intermediate knowledge of UiPath, and is designed to handle common automation tasks efficiently. With its independent configuration setup, it ensures ease of use and reliability in diverse environments.

## Directory Structure

The home directory contains essential files and directories structured as follows:
```
C:.
│ Config.json
│ project.json
│ Readme.md
├───Out
└───Utils
├───Excels
│ Exceptions.xlsx
│ Input File.xlsx
└───Workflows
Adding_Exception.xaml
FrameWork.xaml
```

- **Config.json**: Configuration file for the project settings.
- **project.json**: Stores the project structure.
- **Readme.md**: This readme file.
- **Out**: Directory to store output files generated during execution.
- **Utils**: Directory containing utility files and subdirectories:
  - **Excels**: Holds Excel files needed for execution, such as Exceptions.xlsx and Input File.xlsx.
  - **Workflows**: Contains workflow files (XAML) including Adding_Exception.xaml and FrameWork.xaml.

## Workflows

The Basic Framework includes two primary workflows:

### Framework.xaml

This is the main workflow where execution begins and includes several key parts:

- **Setup Module**: Sets up prerequisites for the process.
  - **Reading Configuration File**: Reads settings from Config.json to make the robot dynamic and application-independent.
  - **Setup inside Try Catch Block**: Ensures robust setup and handles exceptions.

- **Processing**
  - Process data iteratively from an Excel file. Handles exceptions for each row using try/catch blocks and continues with the next record.
 
    ![processing](https://github.com/AnkRaw/UiPath-Basic-Framework/assets/45765236/97f911c1-7bcd-4a62-91aa-cd04d52f4be9)


- **Setup Incomplete**
  - Logs if the setup is incomplete.
 
    
![setup](https://github.com/AnkRaw/UiPath-Basic-Framework/assets/45765236/3de3b662-0c6c-4513-8765-3a6a0ac21f63)

- **Tear Down**
  - Closes all dependencies.
 
    
    ![tear_down](https://github.com/AnkRaw/UiPath-Basic-Framework/assets/45765236/e40d8a6e-f8eb-4848-9b14-bf2534eeefcf)


### Adding_Exception.xaml

Handles all exceptions by logging related information, making error tracking and resolution easier.


![exceptions_workflow](https://github.com/AnkRaw/UiPath-Basic-Framework/assets/45765236/f52c247a-1d3d-4726-91ee-a1d4ddc1d33a)


## Usage

### Clone the Repository

```sh
git clone https://github.com/yourusername/uipath-basic-framework.git
```
### Open in UiPath Studio
Open the project folder in UiPath Studio.

### Modify Config.json
Update Config.json with your specific settings.

### Run the Framework
Execute project.json or FrameWork.xaml in UiPath Studio.

## Contributing
Contributions are welcome! Please fork this repository and submit pull requests for any improvements or bug fixes.
Contributions are welcome! Please fork this repository and submit pull requests for any improvements or bug fixes.
