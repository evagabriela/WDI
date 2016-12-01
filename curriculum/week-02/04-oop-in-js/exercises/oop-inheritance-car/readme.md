#Bodyshop Part 2

Cars are great and all, but now it's time to extend this system and make it handle more types of vehicles.

## Instructions

1. Fork and clone the repository
1. Change into the new directory.
1. Create a working branch, `challenge`.
1. Follow the remaining instructions.

## Requirements

###Part 1 -- Trucks

Create a new constructor called `Truck` that inherits `Car`.

This should be done in the file called `Truck.js`, which requires `Car.js` for you to use.

Your `Truck` constructor should meet the following requirements.

* Must be an instance of `Truck`
* Must be an instance of `Car`.
* Must have the following constructor parameters:
  * make
  * model
  * year
  * color
  * passengers
* Must default to 3 seats.

###Part 2 -- Motorcycles

Create a new constructor called `Motorcycle` that inherits your `Car` constructor.

This should be done in the file called `Motorcycle.js`, which requires `Car.js` for you to use.

Your `Motorcycle` constructor should meet the following requirements.

* Must be an instance of a `Motorcycle`
* Must be an instance of a `Car`
* Must have the following parameters
  * make
  * model
  * year
  * color
  * passengers
* Must default to 2 seats
* Must be able to do a wheelie by calling `wheelie()`, but only if running.
  * If the wheelie is successful, return true and `console.log` the following: `"Doing a sick wheelie!!"`. Otherwise return false.
  * This function should be attached to `Motorcycle.prototype`.

---

## Licensing
1. All content is licensed under a CC-BY-NC-SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.
