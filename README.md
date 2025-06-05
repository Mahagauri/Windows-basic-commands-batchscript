# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
Developed By: Mahagauri P                                                                                                                                                                                
Reg.No: 212224040181
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
```bat
mkdir my-folder
```
![image](https://github.com/user-attachments/assets/45b8a92c-15cb-4c22-9dea-c143a195c5eb)

Remove the directory "my-folder"

## COMMAND AND OUTPUT
```bat
rmdir my-folder
```
![image](https://github.com/user-attachments/assets/c5af845d-30d6-4bf9-97a5-6c03fde8e0b1)

Create the file Rose.txt

## COMMAND AND OUTPUT
```bat
COPY CON Rose.txt
A clock in a office can never get stolen
Too many employees watch it all the time
^Z

dir Rose.txt
```
![image](https://github.com/user-attachments/assets/eab0fb67-175f-4582-b362-39fdc9a91bab)


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
```bat
echo “Hello World” > hello.txt
type hello.txt
```
![image](https://github.com/user-attachments/assets/834d5434-908c-49f9-b861-028b6514165a)

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
```bat
copy hello.txt hello1.txt
type hello1.txt
```
![image](https://github.com/user-attachments/assets/8f1ddebe-1450-456c-a2dd-93e9ef193d35)

Remove the file hello1.txt &                                                                                                                                                                                
List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
```bat
del hello1.txt
dir hello1.txt
```
![image](https://github.com/user-attachments/assets/1718bc75-f6c1-440f-b91d-dfcaace1d880)

List out all the associated file extensions 

## COMMAND AND OUTPUT
```bat
assoc | more
```
![image](https://github.com/user-attachments/assets/0f72bdec-0175-401b-9e02-181635bcb780)

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
```bat
fc hello.txt Rose.txt
```
![image](https://github.com/user-attachments/assets/e580894b-21d0-4dcd-8523-f159dbdb0b98)

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```bat
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT
![image](https://github.com/user-attachments/assets/2710e6e9-345d-4c2d-8481-78c14db964c6)



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```bat
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```

## OUTPUT
![image](https://github.com/user-attachments/assets/73e0aaa9-641a-4dc5-bb67-d02eecb0c665)

Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```bat
@echo off
for %%i in (1,2,3,4,5) do (
    echo Number: %%i
)
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/e3809057-0aed-4ca1-821e-d292451610bd)


Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```bat
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/946f917c-3157-4697-b2f9-e7862bf19d8e)


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```bat
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option:
if %choice"=="1" goto hello
if %choice"=="2" goto createfile
if %choice"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu

:end
echo Goodbye!
pause
```

## OUTPUT
![image](https://github.com/user-attachments/assets/a3cdde33-36ec-4208-8731-da2a1f394e9a)

# RESULT:
The commands/batch files are executed successfully.

