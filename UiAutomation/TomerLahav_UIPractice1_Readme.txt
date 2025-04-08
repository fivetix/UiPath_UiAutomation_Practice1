Readme - Extract invoice details.

Description:

This automation extracts invoice details by the following  steps:
    1.Reads an input Excel file containing invoice numbers.
    2.Signs in to the AMCE website.
    3.Navigates to the invoice search page and searches for each invoice number.
    4.Extracts invoice details and writes them back to the Excel file. 

Requirements:

1.UiPath Studio installed
2.The following UiPath packages:
	UiPath.Excel.Activities
	UiPath.System.Activities
	UiPath.UIAutomation.Activities
3.UiPath Edge Extension installed
4.Microsoft Edge browser installed

Project Files:

1.TomerLahav_UIPractice1_ExtactInvoiceDetails.xaml - the main UiPath workflow
2.TomerLahav_UIPractice1_Input.xlsx - input file containing invoice numbers

How to Run the Project:

1.Open the .xaml file in UiPath Studio.
2.Ensure that TomerLahav_UIPractice1_Input.xlsx is inside the project folder.
3.Make sure the TomerLahav_UIPractice1_Input.xlsx file is closed before running.
4.Click Run to start the automation.

Additional Notes:

1. The robot logs out from the website at the end of the automation for security reasons. If the user was already logged in before the automation started, the robot will take 6 seconds before proceeding to the next screen.

2. The automation handles invalid invoice numbers: If an invoice number is not found, the robot logs an error message and moves on to the next row in the Excel file. If there is an empty row the robot do notice it and skips to the next row with printing a log msg. 
