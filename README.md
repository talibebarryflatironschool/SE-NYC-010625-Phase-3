# Lecture # 4 - OOP Part 2: Class Methods & Class Variables

## Lecture Topics

- Class variables
- Class methods (`@classmethod`)
- Relative Imports (`from car import Car`)

## Introduction

In today's lecture, we will discuss more topics of Object Oriented Programming in Python including class variables and class methods.

## Setup

1. Make sure that your current working directory (folder) contains a `Pipfile`, then run `pipenv install` in your terminal to install `pytest` and any other required packages.

2. Now that your `pipenv` virtual environment is ready to use, run `pipenv shell` in your terminal to enter the virtual environment.

3. Run `pytest` to run the tests.

## Deliverables

Write your code in `lib/debug.py` for Deliverable # 1 (the `debug.py` file in the `lib` directory / folder)

1. Write the following code to import the `Car` class from the `car.py` file into `debug.py`:

```python
from car import Car
```

Write your code in `lib/car.py` for Deliverables # 2 - 4 (the `car.py` file in the `lib` directory / folder)

2. Create a property for the `model` instance variable. For the setter method, the `model` cannot be changed after it is initialized and must be a `str`. If the `model` instance variable already exists and there is an attempt to change its value, or if the value is not a `str`, raise an `Exception` with the message `"Model cannot be changed and must be a string!"`.

   - Hint: Use the `hasattr()` function to check for the presence of an attribute within an instance.

3. Create a class attribute, `all`. We will use this attribute to keep track of the new `Car` instances that are created from the `Car` class. Set this attribute equal to `[]`. Then in `__init__`, you will need to append the new `Car` instances to the list contained within the `all` class attribute for the `Car` class.

4. Create a class method, `average_year()` that will return the average year for all cars created.