# Coffee Machine Project

This project simulates a simple coffee machine that can make espresso, latte, and cappuccino. The machine checks if there are enough resources to make the selected drink, processes coin payments, and updates its resources accordingly.

## Table of Contents

- [Features](#features)
- [Menu](#menu)
- [Resources](#resources)
- [Profit](#profit)
- [Functions](#functions)
  - [is_resource_sufficient(order_ingredients)](#is_resource_sufficientorder_ingredients)
  - [process_coins()](#process_coins)
  - [is_transaction_successful(money_received, drink_cost)](#is_transaction_successfulmoney_received-drink_cost)
  - [make_coffee(drink_name, order_ingredients)](#make_coffeedrink_name-order_ingredients)
- [Usage](#usage)
- [Example](#example)
- [License](#license)

## Features

- **Make Coffee:** The machine can make espresso, latte, and cappuccino.
- **Resource Checking:** The machine checks if there are enough resources before making a drink.
- **Coin Processing:** The machine processes coin payments and gives change if necessary.
- **Resource Reporting:** The machine can report its current resource levels and profit.

## Menu

The coffee machine offers the following drinks:

| Drink      | Cost | Ingredients                                |
|------------|------|--------------------------------------------|
| Espresso   | $1.50| 50ml water, 18g coffee                     |
| Latte      | $2.50| 200ml water, 150ml milk, 24g coffee        |
| Cappuccino | $3.00| 250ml water, 100ml milk, 24g coffee        |

## Resources

The initial resources available in the coffee machine are:

- **Water:** 300ml
- **Milk:** 200ml
- **Coffee:** 100g

## Profit

The initial profit is $0.00.

## Functions

### `is_resource_sufficient(order_ingredients)`

Checks if there are enough resources to make the selected drink.

- **Parameters:** 
  - `order_ingredients` (dict): Ingredients required for the selected drink.
- **Returns:** 
  - `bool`: `True` if resources are sufficient, `False` otherwise.

### `process_coins()`

Processes the coin input from the user and calculates the total amount of money inserted.

- **Returns:** 
  - `float`: The total amount of money inserted.

### `is_transaction_successful(money_received, drink_cost)`

Checks if the inserted money is sufficient to buy the selected drink. If so, it updates the profit and returns change.

- **Parameters:** 
  - `money_received` (float): The amount of money inserted by the user.
  - `drink_cost` (float): The cost of the selected drink.
- **Returns:** 
  - `bool`: `True` if the transaction is successful, `False` otherwise.

### `make_coffee(drink_name, order_ingredients)`

Updates the resources after making a drink and prints a message to the user.

- **Parameters:** 
  - `drink_name` (str): The name of the selected drink.
  - `order_ingredients` (dict): Ingredients required for the selected drink.

## Usage

To run the coffee machine, execute the script. The machine will prompt the user to select a drink or perform other actions.

1. **Select a Drink:** Enter `espresso`, `latte`, or `cappuccino` to make a drink.
2. **Report Resources:** Enter `report` to print the current resource levels and profit.
3. **Turn Off Machine:** Enter `off` to turn off the machine.

## Example

```sh
What would you like? (espresso/latte/cappuccino): latte
Please insert coins.
how many quarters?: 10
how many dimes?: 0
how many nickels?: 0
how many pennies?: 0
Here is $0.0 in change.
Here is your latte ☕️. Enjoy!
