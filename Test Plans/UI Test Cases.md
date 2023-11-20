### Helpful test cases to consider when testing a User Interface

## Required Fields 
If the screen required data entry on a specific field, it is good practice to identify the required fields with a red asterisk and to give a friendly warming if the data is left blank.

## Data Type Errors 
If the screen contains dates, numeric, currency or other specific data types, ensure that only valid data can be entered.

## Field Widths 
If the screen contains text boxes that allow data entry, ensure that the width of data entered does not exceed the width of the table field
example: A title that allows 100 characters in the database should not allow more than 100 characters to be entered from the front-end UI

## On-screen Instructions 
Any screen that is not self-explanatory to the casual user should contain on-screen instructions that aid the user.

## Keep On-screen Instructions Brief 
While onscreen instruction are great, keep the wording informative and concise.

## Progress Bars 
If the screen takes more than 5 seconds to render results, it should contain a progress bar so that the user understands the page is still processing.

## Same Document Opened Multiple Times 
If the application opens the same document multiple times, it should append a unique number to the open document to keep one document from overwriting another.
example: If your application opens a document named ScopeOfWork.md, if it opens the same document for the same user again, consider having it append the time to the document or sequentially number it (e.g., ScopeOfWork2.md or ScopeOfWork_11202023.md).

## Cosmetic Inconsistencies 
The screen look, feel and design should match the other screens in the application. Creating and using a style guide is a great way to ensure consistency throughout the application.

## Abbreviation Inconsistencies 
If your screens contain abbreviations (e.g., Num for Number, Amt for Amount), the abbreviations should be consistent for all screens in the application. The style guide would be used here as well.

## Save Confirmations
If the screen allows changing of data without saving, it should prompt you to save if you move away from this screen.

## Delete Confirmations 
If a person deletes an item, it is a good idea to confirm the delete. However, if the user interface uses combo boxes (drop down lists), be sure to include type ahead (if there are hundreds of items in a list, and the user types in the first letter it will skip to the first item that begins with that letter).

## Grammar and Spelling 
Ensure that you have test cases that look for grammar or spelling errors.

## Table Scrolling 
If the application lists information in table format, if the data in the table extends past one page, the scrolling should scroll the data but leave the table headers in tact.

## Error Logging 
If fatal errors occur as users use the application, ensure that the application writes those errors to a log file, event viewer or a database table for later review. Log the routine the error was in, the person logged on, and the date/time of the error.

## Error Messages 
Ensure that error messages are informative, grammatically correct, and not condescending.

## Shortcuts 
If the application allows short cut keys (e.g., CTRL+S to save), test each shortcut to ensure it works in all different browsers (if the application is web based).

## Invalid Choices 
Do not include instructions for choices not available at the time.
example: If a screen cannot be printed due to the state of data, the screen should not have a print button.

## Invalid Menu Items 
Do not show menu items that are not available for the context of the page you're on.

## Dialog Box Consistency 
Use a style guide to document what choices are available for dialog boxes. There should not be a Save/Cancel dialog on the screen and an OK/Cancel on another, this is inconsistent.
