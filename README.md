# Working with Strings

## Step 1
We can modify the `cout` statements from Lab 2.1 to use `string` variables that hold the values of your first name, last name, zodiac sign, favorite color, and favorite animal. Notice the `#include` directive for `string` has been added towards the top in main.cpp.

To get started, a solution for Lab 2.1 has been provided in the code editor. Now add the necessary variables and modify the `cout` statements. For example, to print your name you could use statements similar to:

**string firstName = "Hector";
string lastName = "Garcia";
cout << "Programmer:  " << firstName + " " + lastName << endl;**

# Step 2

Now instead of hard coding the string values, let's allow the user to provide the input from the keyboard. Add a prompt for each of the string variables asking for an input. The example from Step 1 could now be changed to:

**string firstName, lastName;
cout << "Enter first name:\n";
cin >> firstName;
cout << "Enter last name:\n";
cin >> lastName;
cout << "Programmer:  " << firstName + " " + lastName << endl;**

# Step 3

To allow users to enter strings from the keyboard that contain whitespace characters (like spaces and tabs) we cannot use the method shown in Step 2. One way to allow user input with whitespace characters is to use the `getline` function. Here is how we could modify the example from Step 2 to allow both the user's first and last name to be entered into the same string:

**string name;
cout << "Enter first and last name:\n";
getline(cin, name);
cout << "Programmer:  " << name << endl;**

Modify your program so that the prompt for the user's name will support spaces. For example:

**Enter first and last name:
Hector Garcia**

Important Note: Mixing `cin >>` and `getline` statements can cause unexpected results. If you need to use `getline` after having previously used `cin >>` statements, you should first clear the input buffer using this statement:

cin.ignore(numeric_limits<streamsize>::max(), '\n');