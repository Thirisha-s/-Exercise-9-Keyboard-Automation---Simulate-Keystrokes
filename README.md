# -Exercise-9-Keyboard-Automation---Simulate-Keystrokes

## Aim:
To simulate typing and keyboard shortcuts in a desktop application (Notepad) using Start Process, Type Into, and Send Hotkey activities in UiPath Studio.

## Equipment Required:
UiPath Studio installed on your computer.
Notepad application (pre-installed on Windows).
Computer with:
Minimum 4 GB RAM.
Minimum 2.0 GHz CPU.
Windows operating system.
## Procedure:
Create a New Process in UiPath Studio:
Open UiPath Studio and create a new project by selecting Process under the New Project tab.
Name the process (e.g., Notepad Automation) and click Create.

## Start the Notepad Application:
Search for the Start Process activity in the Activities panel and drag it into the Main sequence.
In the FileName property of Start Process, enter the path to the Notepad executable (notepad.exe):
```
notepad.exe
```
This activity will launch Notepad when the automation runs.
Simulate Typing Text into Notepad:
After launching Notepad, use the Type Into activity to simulate typing.
Drag the Type Into activity into the sequence under the Start Process activity.
Click Indicate on Screen and select the main text area of Notepad.
In the Text property, enter the text you want to simulate typing, such as:
```
This is a sample text.
```
Make sure to check the SimulateType option in the Properties panel for faster, invisible typing.

## Simulate Save Shortcut (Ctrl + S):
To simulate the Save keyboard shortcut (Ctrl + S), use the Send Hotkey activity.
Drag the Send Hotkey activity below the Type Into activity.
Click Indicate on Screen and select the Notepad window again.
Set the Key property to Ctrl + S, which will open the Save As dialog.

## Simulate Typing the File Name:
After pressing Ctrl + S, the Save As dialog will appear where you can type the file name.
Use another Type Into activity to enter the filename.
Click Indicate on Screen and select the filename input field in the Save As dialog box.
In the Text property, enter the desired file path and name.
Check the SimulateType option to type the filename faster.

## Press Enter to Save the File:
To confirm saving, use another Send Hotkey activity for the Enter key.
Drag the Send Hotkey activity under the Type Into activity for the filename.
Click Indicate on Screen and select the Save As dialog box.
Set the Key property to Enter, which will save the file.

## Save and Run the Workflow:
Press CTRL+S to save the workflow.
Click the Run button to execute the automation.
UiPath will launch Notepad, type the text, save the file, and close the application automatically.
## UiPath WorkFlow:
![Screenshot 2024-09-27 183914](https://github.com/user-attachments/assets/429974bd-73e2-47d4-ac89-dce803b02bba)
![Screenshot 2024-09-27 183958](https://github.com/user-attachments/assets/8ed3febb-a8af-4719-8210-c4e4c6fc91c3)
![Screenshot 2024-09-27 184314](https://github.com/user-attachments/assets/06fdac66-7e1e-4f40-ae69-0bca26ffd957)
![Screenshot 2024-09-27 190008](https://github.com/user-attachments/assets/c557e889-ec36-418a-9353-c19aa0f9ac70)


## Result:
The text is typed into Notepad, saved with a given filename, and Notepad is closed using keyboard shortcuts, all simulated through UiPath automation.
