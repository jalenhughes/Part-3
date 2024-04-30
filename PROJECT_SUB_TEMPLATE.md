# Project Part 3

## Requirments 
1. Funcations:
- Write a function for each of the menu options you previously created.
- You must include at least one of each of the following:
   - A value returning function
   - A void function
   - A pass by reference function that changes the value in the function (remember arrays are automatically passed by reference)
- You must use function prototypes.
2. Arrays/Vectors:
- Expand your data set to include more records (minimum 10)
- Store your values in parrallel arrays or vectors
- In your analysis of specificaction explain why you choose an array or vector over the other.


## Table of Contents
1. [Statement of Independent Effort](#statement-of-independent-effort)
1. [Analysis of Specifications](#analysis-of-specifications)
    - [Main](#main)
1. [Pseudocode](#pseudocode)
1. [Flowchart](#flowchart)
1. [Test Cases](#test-cases)
1. [Code](#code)
1. [User Manual](#user-guide)
1. [References](#references)

## Statement of Independent Effort


I, ***Jalen Hughes***, hereby certify that is my original work completed without the assistance of anyone or any outside resources.


## Analysis of Specifications

### Main

| Input    | Process  | Output   |
| -------- | -------- | -------- |
| Car Type (1 or 2)|Collecting Car Information| End of Program  Details saved to  car_cart.txt.   |
Car Make (1 or 2)|Checking Car Make and Model
 Car Model|Mileage Check
 Car Mileage|File Output 
 -|Repeating the Process|
 -|Error Handling|
## Pseudocode
```
BEGIN

CONSTANT PI = 3.14159

FUNCTION displayMenu():
    OUTPUT "Welcome to the car depot!"
    OUTPUT "Do you want to get a car? (y/n):"

FUNCTION getInput(prompt: String) -> String:
    OUTPUT prompt
    INPUT input
    RETURN input

FUNCTION getIntInput(prompt: String) -> Integer:
    OUTPUT prompt
    INPUT input
    RETURN input

PROCEDURE addVehicle(types: List[String], makes: List[String], models: List[String], mileages: List[Integer]):
    BEGIN
        DECLARE carType: String
        DECLARE carMake: String
        DECLARE carModel: String
        DECLARE carMileage: Integer
        
        carType = getInput("What type of car is it? (Trucks/Cars): ")
        types.ADD(carType)

        carMake = getInput("What Make of cars would you like? (Toyota/Kia): ")
        makes.ADD(carMake)

        carModel = getInput("What model of " + carMake + " would you like? ")
        models.ADD(carModel)

        carMileage = getIntInput("Input car mileage: ")
        mileages.ADD(carMileage)
    END

BEGIN
    DECLARE types: List[String]
    DECLARE makes: List[String]
    DECLARE models: List[String]
    DECLARE mileages: List[Integer]
    DECLARE choice: String

    displayMenu()
    choice = getInput("Do you want to get a car? (y/n): ")

    WHILE choice == "y" OR choice == "Y" DO
        BEGIN
            addVehicle(types, makes, models, mileages)

            choice = getInput("Do you want to get another car? (y/n): ")
        END

    FOR i = 0 TO types.LENGTH - 1 DO
        BEGIN
            IF mileages[i] < 100000 THEN
                OUTPUT "Vehicle -", types[i], makes[i], models[i], "with mileage", mileages[i], "added to the cart."
            ELSE
                OUTPUT "Vehicle mileage is over 100,000. Not eligible for test drive."
        END

    OUTPUT "End of test driving vehicles."
END
```




## Flowchart

_Paste flowchart image here. Note that the image has to uploaded to your repository and then a link added here_


## Test Cases

|Case #|Case Description|Input|Condition (Mileage < 100000)|Output|
|:---:|:---|:---|:---:|:---| 
|1|Item that should be approved|Mileage < 100000 |True|Vehicle - with mileage added to cart|
|2|Item that should not be approved|Mileage > 100000|False|Vehicle mileage is over 100,000. Not eligible for test drive.|
|3|Item that should not be approved|Mileage = 10000|False| Vehicle mileage is over 100,000. Not eligible for test drive.|
|4|Item that should be approved|Mileage = 99999 |True|Vehicle - with mileage added to cart|
|5|Item that should be approved|Mileage = -100000 |True|Vehicle - with mileage added to cart|


## Code

```cpp
#include <iostream>
#include <fstream>
#include <string>

using namespace std;

// Function prototypes
void displayMenu();
string getInput(string prompt);
int getIntInput(string prompt);
void addVehicle(string carType, string carMake, string carModel, int mileage, ofstream& outFile);

int main() {
    string carType;
    string carMake;
    string carModel;
    int mileage;
    char choice;

    ofstream outFile("car_cart.txt");

    if (!outFile) {
        cerr << "Error opening file." << endl;
        return 1;
    }

    displayMenu();
    cin >> choice;

    while (choice == 'y' || choice == 'Y') {
        carType = getInput("What type of car is it? (Trucks/Cars): ");
        carMake = getInput("What Make of cars would you like? (Toyota/Kia): ");
        carModel = getInput("What model of " + carMake + " would you like? ");
        mileage = getIntInput("Input car mileage: ");

        addVehicle(carType, carMake, carModel, mileage, outFile);

        cout << "Do you want to get another car? (y/n): ";
        cin >> choice;
    }

    outFile.close();
    cout << "End of test driving vehicles. Details saved to car_cart.txt." << endl;

    return 0;
}

void displayMenu() {
    cout << "Welcome to the car depot!" << endl;
    cout << "Do you want to get a car? (y/n): ";
}

string getInput(string prompt) {
    string input;
    cout << prompt;
    cin.ignore(); // Ignore previous newline character
    getline(cin, input);
    return input;
}

int getIntInput(string prompt) {
    int input;
    cout << prompt;
    cin >> input;
    return input;
}

void addVehicle(string carType, string carMake, string carModel, int mileage, ofstream& outFile) {
    if (mileage < 100000) {
        cout << "Vehicle - " << carType << " " << carMake << " " << carModel << " with mileage " << mileage << " added to the cart." << endl;
        outFile << "Vehicle - " << carType << " " << carMake << " " << carModel << " Mileage: " << mileage << endl;
    } else {
        cout << "Vehicle mileage is over 100,000. Not eligible for test drive." << endl;
    }
}


```

## User Manual
_Include a link to a separate file called GUIDE.md_

[User Manual](GUIDE.md) <br/>
_Updated: **[DATE]**_

## Getting Started
To use the program, follow these steps:

* Compile and run the provided C++ code in your preferred Integrated Development Environment (IDE) or compiler.
* Upon running the program, you will be prompted with a series of questions to input details about the vehicles you are interested in.


_List all references in [APA 7 Format](https://owl.purdue.edu/owl/research_and_citation/apa_style/apa_formatting_and_style_guide/index.html)._
