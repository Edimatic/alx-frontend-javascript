#	ES6 Classes

This project contains tasks for learning to use classes in ECMAScript 2015 (ES6).

##	Tasks To Complete

###	0. You used to attend a place like this at some point
0-classroom.js contains a script that exports a class named ClassRoom with the following requirements:

    Prototype: export default class ClassRoom.
    It should accept one attribute named maxStudentsSize (Number) and assigned to _maxStudentsSize.


###	1. Let's make some classrooms
1-make_classrooms.js contains a script that meets the following requirements:

    Import the ClassRoom class from 0-classroom.js.
    Export a function named initializeRooms. It should return an array of 3 ClassRoom objects with the sizes 19, 20, and 34 (in this order).


###	2. A Course, Getters, and Setters
2-hbtn_course.js contains a script that exports a class named HolbertonCourse with the following requirements:

    Constructor arguments:
        name (String).
        length (Number).
        students (array of Strings).
    Make sure to verify the type of attributes during object creation.
    Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
    Implement a getter and setter for each attribute.


###	3. Methods, static methods, computed methods names..... MONEY
3-currency.js contains a script that exports a class named Currency with the following requirements:

    Constructor arguments:
        code (String).
        name (String).
    Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
    Implement a getter and setter for each attribute.
    Implement a method named displayFullCurrency that will return the attributes in the format name (code).


###	4. Pricing
4-pricing.js contains a script that meets the following requirements:

    Import the class Currency from 3-currency.js.
    Export a class named Pricing that meets the following requirements:
        Constructor arguments:
            amount (Number).
            currency (Currency).
        Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
        Implement a getter and setter for each attribute.
        Implement a method named displayFullPrice that returns the attributes in the format amount currency_name (currency_code).
        Implement a static method named convertPrice. It should accept two arguments: amount (Number), conversionRate (Number). The function should return the amount multiplied by the conversion rate.


###	5. A Building
5-building.js contains a script that exports a class named Building with the following requirements:

    Constructor arguments:
        sqft (Number).
    Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
    Implement a getter for each attribute.
    Consider this class as an abstract class. And make sure that any class that extends from it should implement a method named evacuationWarningMessage.
        If a class that extends from it does not have a evacuationWarningMessage method, throw an error with the message Class extending Building must override evacuationWarningMessage.


###	6. Inheritance
6-sky_high.js contains a script that meets the following requirements:

    Import Building from 4-building.js.
    Export a class named SkyHighBuilding that extends from Building and meets the following requirements:
        Constructor arguments:
            sqft (Number) (must be assigned to the parent class Building).
            floors (Number).
        Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
        Implement a getter for each attribute.
        Override the method named evacuationWarningMessage and return the following string Evacuate slowly the NUMBER_OF_FLOORS floors.


###	7. Airport
7-airport.js contains a script that exports a class named Airport with the following requirements:

    Constructor arguments:
        name (String).
        code (String).
    Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
    The default string description of the class should return the airport code (example below).


###	8. Primitive - Holberton Class
8-hbtn_class.js contains a script that exports a class named HolbertonClass with the following requirements:

    Constructor arguments:
        size (Number).
        location (String).
    Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
    When the class is cast into a Number, it should return the size.
    When the class is cast into a String, it should return the location.


###	9. Hoisting
9-hoisting.js contains a fixed and working copy of the code below:

const class2019 = new HolbertonClass(2019, 'San Francisco');
const class2020 = new HolbertonClass(2020, 'San Francisco');

export class HolbertonClass {
  constructor(year, location) {
    this._year = year;
    this._location = location;
  }

  get year() {
    return this._year;
  }

  get location() {
    return this._location;
  }
}

const student1 = new StudentHolberton('Guillaume', 'Salva', class2020);
const student2 = new StudentHolberton('John', 'Doe', class2020);
const student3 = new StudentHolberton('Albert', 'Clinton', class2019);
const student4 = new StudentHolberton('Donald', 'Bush', class2019);
const student5 = new StudentHolberton('Jason', 'Sandler', class2019);

export class StudentHolberton {
  constructor(firstName, lastName) {
    this._firstName = firstName;
    this._lastName = lastName;
    this._holbertonClass = holbertonClass;
  }

  get fullName() {
    return `${this._firstName} ${this._lastName}`;
  }

  get holbertonClass() {
    return this.holbertonClass;
  }

  get fullStudentDescription() {
    return `${self._firstName} ${self._lastName} - ${self._holbertonClass.year} - ${self._holbertonClass.location}`;
  }
}


export const listOfStudents = [student1, student2, student3, student4, student5];


###	10. Vroom
10-car.js contains a script that exports a class named Car with the following requirements:

    Constructor arguments:
        brand (String).
        motor (String).
        color (String).
    Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
    Add a method named cloneCar. This method should return a new object of the class.


###	11. EVCar
100-evcar.js contains a script that meets the following requirements:

    Import Car from 10-car.js.
    Export a class named EVCar that extends the Car class and meets the following requirements:
        Constructor arguments:
            brand (String).
            motor (String).
            color (String).
            range (String).
        Each attribute must be stored in an "underscore" attribute version (ex: name is stored in _name).
        For privacy reasons, when cloneCar is called on an EVCar object, the object returned should be an instance of Car instead of EVCar.
