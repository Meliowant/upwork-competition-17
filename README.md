# Assignment Django Starter Template

## Summary
We are a local home cleaning company called Homework. Today we are keeping track of all our bookings using a spreadsheet and we want to move it into a web application instead using Django. Our main goal with this project is to make it possible for customers to schedule a booking online. I've already created the scaffolding of the app for you and now I need you to add some functionality to it. This should take you about 1-2 hours, but you have up to 4 hours to complete it.

### Deliverables
1. All models and columns should have validation as described in the model spec below.
2. Currently we operate in 10 cities, but plan to expand quickly. We need a way to store the list of cities we operate in and the ability to add to the list. You should create a new table to do this.
3. On the Cleaner Form we need a way to select the cities a cleaner works in. This should be a checkbox list populated by the list of cities we operate in. You may need to need to create a new table to store this data.
4. We need a way for customers to signup and schedule a booking all on one form. To accomplish this you will need to do the following:
  - Create a new root page for the application with a form designed for customers to signup and create a booking.
  - On this form, capture all the data needed to create a customer in the database (first name, last name, phone number).
  - If the customer already exists in the database (use phone number to determine this) use the existing record instead of creating a new one. You should probably add a validation to enforce this.
  - Let the customer select what city they are in from the cities table created earlier.
  - Let the customer specify a date and time when they would like their house cleaned.
  - When the user submits the form, look for cleaners that work in the specified city that do not have any bookings that conflict with the time specified.
  - If you can find an available cleaner, create the booking and display the name of the cleaner assigned to the booking.
  - If you can't find an available cleaner, tell the user that we could not fulfill their request.
5. Write tests for the parts of the application you feel need it the most.
6. When you are done, please zip up the whole app directory with dependencies and upload it below.

### Models
- customer
  - first_name (required)
  - last_name (required)
  - phone_number (optional)
- booking
  - customer (required)
  - cleaner (required)
  - date (required)
- cleaner
  - first_name (required)
  - last_name (required)
  - quality_score (required, must be a number between 0.0 and 5.0)
### Restrictions
Do not remove git from your application directory.


#### Note:
Please use `python-3.5.1`

## Installation

#### 1.
You should already know what is [virtualenv](http://www.virtualenv.org/). So, simply create it for your own enviroment.
````bash
$ mkdir ~/.virtualenvs
$ python3 -m venv ~/.virtualenvs/cleaners
$ source ~/.virtualenvs/cleaners/bin/activate
````
#### 2.
The *requirements.txt* file  has all the great debugging tools, django helpers and some other cool stuff. To install them, simply type:

`$ pip install -r requirements.txt`
