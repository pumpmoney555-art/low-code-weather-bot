Low-Code Weather Bot
This repository contains the UiPath automation project developed as a group assignment for the Low-Code Development course. The automation aims to extract city names from an Excel file, retrieve the current temperature from Google Search, and update the Excel file with the corresponding temperatures.

Project Objective
The primary objective of this automation is to streamline the process of gathering current temperature data for a list of cities, eliminating the need for manual searching and data entry.

User Stories
• As a data analyst, I want to automate temperature retrieval for city names, so that I can quickly update my reports without manual effort.
• As a report manager, I want to ensure that the data in my reports is always up-to-date, so that I can make informed decisions based on the latest information.

Automation Workflow
The UiPath automation performs the following steps:

1.Reads City Names: Reads a list of city names from Column A of an Excel file.
2.Opens Google: Navigates to Google Search in the Edge browser.
3.Searches Temperature: For each city, it types a search query (e.g., "temperature in [city name]") into Google Search and presses Enter.
4.Extracts Temperature: Extracts the current temperature from the Google Search results page.
5.Updates Excel: Writes the extracted temperature into Column B of the same row in the Excel file.
6.Saves and Closes: Saves and closes the updated Excel file.

Test Plan
The automation's functionality was verified through the following test cases:

• Test Case 1: Verify that the Excel file loads correctly.
• Test Case 2: Check if the automation correctly searches Google for weather data for each city.
• Test Case 3: Confirm that the extracted temperature is accurately written in Column B of the Excel file.

Compliance and Controls
• Data Privacy: The automation handles publicly available, non-sensitive data.
• Logging: The automation includes basic logging to record the execution flow and potential errors.
• Exception Handling: The automation includes basic exception handling to manage scenarios such as invalid city names or inability to retrieve temperature data.

Variables
Variable Name	Type	Purpose
dt_Cities	System.Data.DataTable	Stores the data read from the input Excel file.
str_Temperature	String	Temporarily stores the extracted temperature as a string.
CurrentRow	System.Data.DataRow	Represents the current row being processed in the data table.

Getting Started
To run this automation:

1.Ensure you have UiPath Community Edition installed.
2.Download or clone this repository to your local machine.
3.Open the Main.xaml file in UiPath Studio.
4.Make sure the input Excel file (with city names in Column A) is located in the project folder or update the file path in the Use Excel File activity.
5.Run the Main.xaml workflow.
