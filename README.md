Cooking With Ansible
====================

In this project there are two vars files:

- shoppinglist.yml
  - A list of items we want to buy
- store-inventory.yml
  - An inventory from the store of items they have in stock

Build an ansible playbook that will output a list of the items we can buy based on the available inventory, omitting the items that don't have enough stock. 

The store doesn't have enough stock for our list, so the output will be a subset of these items.