# Part 3 Guide

_Author: **Jalen Hughes**_ <br/>
_Version: **3**_ <br/>
_Revised: **03/10/24**_ <br/>
<small>Copyright (C)**[CURRENT YEAR]**, <i>All rights reserved.</i></small>

[//]: <> (User Guide Samples: https://www.dropbox.com/scl/fo/l4cwcd61u2k6n8w6ovbzu/h?rlkey=djxdqkmyexvbw7jcdao6u2hlg&dl=1)

## Table of Contents

1. [Introduction](#introduction)
2. [Major Features](#major-features)

## Introduction
This code simulates a simplified car depot system where users can interactively select and add vehicles to a virtual shopping cart. The program prompts users to input details about the type of car they want (Trucks/Cars), the make of the car (Toyota/Kia), the specific model based on the make, and the car's mileage. It then checks if the mileage is below 100,000 and adds the vehicle details to a list if it is eligible for a test drive.

The code includes functions for displaying the main menu, getting string input, getting integer input, and adding a vehicle to the lists. It uses parallel lists (types, makes, models, mileages) to store the details of multiple vehicles. The program also includes error handling for invalid input and ensures a smooth user experience by looping through the menu options until the user chooses to stop adding vehicles.

Overall, this code demonstrates the flow of a simple interactive program that manages vehicle selection and test drive eligibility based on user inputs.

## Major Features
_List and describe the major features of your application._

1. **Interactive Menu:** The application presents an interactive menu to the user, allowing them to choose whether they want to get a car.
2. **User Input Handling:** It handles user input for selecting the type of car (Trucks/Cars), the make of the car (Toyota/Kia), the specific model, and the car's mileage. It includes functions for getting both string and integer inputs.
3. **Adding Vehicles:** Users can add multiple vehicles to their shopping cart. The program stores details such as the type, make, model, and mileage of each vehicle in separate lists.
4. **Test Drive Eligibility:** The program checks if the mileage of each vehicle is below 100,000. Vehicles meeting this criterion are added to the cart and displayed as eligible for a test drive.
5. **Output Display:** The application outputs information about the vehicles added to the cart, including their type, make, model, and mileage. It also displays a message if a vehicle is not eligible for a test drive.
6. **Error Handling:** The program includes error handling for invalid input, ensuring that the user provides valid input data.
7. **Looping Structure:** It uses loops (while loop and for loop) to iterate through the menu options, vehicle selection process, and displaying vehicle information, providing a smooth and continuous user experience.
8. **Modular Design:** The code is structured using functions, promoting modularity and code organization. Functions such as displayMenu, getInput, getIntInput, and addVehicle handle specific tasks, making the code more readable and maintainable.
9. **Data Structure Usage:** The application utilizes parallel lists (types, makes, models, mileages) to store and manage data related to multiple vehicles efficiently.

10. **File Closure and Final Message**: After the user is done selecting cars, the output file is closed, and a message is displayed indicating the end of the test-driving session. The details of the selected vehicles are saved in the "car_cart.txt" file.
