# Checklist

Before you submit the final version of your labs, make sure that your project fullfills all of the tasks that will be added to this checklist.

## 00 Introduction

- [X] Install an IDE on your system

## 01 Git

- [X] Fork and clone the 1md031-lab-21 repository

## 02 HTML

Your index.html file contains:
- [X] A headline
- [X] A section to select burgers that contains at least three items. Each item has:
    - [X] A name
    - [X] An image
    - [X] Information about allergies 
- [X] A section to collect customer information:
    - [X] First- and Last Name (in one field)
    - [X] E-Mail Address
    - [X] Street
    - [X] House Number (only allowing numbers in this field)
    - [X] Gender (male, female, do not wish to provide as radio buttons)
- [X] A button to place the order
- [X] Ensure the website loads when opening http://localhost:8080


## 03 CSS

The style.css file contains:
- [X] A rule to make the allergy information bold
- [X] Different text and background color for the two different sections (burger selection and customer information)
- [X] Change the cursor when hovering over the order button
- [X] Adds margins to the sections and the order button
- [X] Add a border to the two sections
- [X] Create a header that places an image behind the headline
- [X] Use a grid layout for the burger selection section



## 04 JavaScript and Vue

- [X] You have a menu.json file which contains at least three different burgers with respective attributes

Your Home.vue file:
- [X] ... contains a MenuItem constructor (that is not used)
- [X] ... loads the information from the menu.json object and inserts the information to the burger selection section
- [X] ... allows the customer to click in the interactive map to select delivery location
- [X] ... has an order button that sends the information from the text boxes, the gender, all items on the order, and the delivery location to the server (to be realyed to the dispatcher)

Your Burger.vue component:
- [X] ... allows adding and removing burgers from the order
- [X] ... only displays allergy information if relevant (either only if it contains gluten or lactose, or only if it's gluten or lactose free)

Your Dispatcher.vue file:
- [X] ... shows for every order :
    - [X] a location on the map
    - [X] the order information
    - [X] the customer information

## Optional
- [ ] Only allow the order to be sent if all necessary information are provided
- [ ] Display receipt on the customer page as well
- [ ] Allow the dispatcher to handle orders by providing buttons next to every order that can switch the order status to "in preparation" and "done"
- [ ] Display the order status to the customer and update it in the customer view if updated by the dispatcher
- [ ] Show the order status for the customer as well.
- [ ] Find a better visualization for what orders belong to which location on the map