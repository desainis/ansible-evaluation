Cooking With Ansible
====================

In this project there are two vars files:

- shoppinglist.yml
  - A list of items we want to buy
- store-inventory.yml
  - An inventory from the store of items they have in stock

Build an ansible playbook that will output a list of the items we can buy based on the available inventory, omitting the items that don't have enough stock. 

The store doesn't have enough stock for our list, so the output will be a subset of these items.

--- 

## Solution

- The solution for this problem is in the `check-inventory.yml` playbook.

### Requirements:
- `Ansible` >= `2.9.7`

### Dependencies

- `shoppinglist.yml`
  - A list of items we want to buy (_Note:_ It is assumed that the shopping list contains a `foods` dictionary following the _given_ schema and it is **not empty**)
- `store-inventory.yml`
  - An inventory from the store of items they have in stock (_Note:_ It is assumed that the store contains a `inventory` array following the _given_ schema and it is **not empty**)

### Download the solution

- Clone this repository and switch directories
  - SSH
    - `git clone git@github.com:desainis/ansible-evaluation.git | cd ansible-evaluation`
  - HTTPS
    - `git clone https://github.com/desainis/ansible-evaluation.git | cd ansible-evaluation`

### Usage

- `ansible-playbook check-inventory.yml`

_Note:_ An implicit localhost warning may appear. Some localhost warnings have been turned off using an option ansible.cfg file.

### Results
- A comma seperated list of available items based on the shopping list and store inventory list is printed _if the result is non-empty_. 