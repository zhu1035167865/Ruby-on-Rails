# Ruby-on-Rails

# Soft Delete Functionality in Ruby on Rails

## Overview

This project implements basic soft delete functionality for a Ruby on Rails model named Item. Soft deletes involve marking records as "deleted" without physically removing them from the database. The implemented functionality includes:

- **Model Creation**: Creation of a new Ruby on Rails model named `Item` with attributes `name` (string) and `deleted_at` (datetime).
  
- **Soft Delete Mechanism**: Implementation of a soft delete mechanism using the `deleted_at` attribute. The model includes methods:
  - `soft_delete`: Updates the `deleted_at` attribute with the current timestamp.
  - `restore`: Sets the `deleted_at` attribute to `nil`.

- **Default Scope**: A default scope is included in the `Item` model to exclude "deleted" items from normal queries.

- **Testing**: RSpec tests are provided to ensure the correct functionality of soft delete, restoration, and the default scope.

**Install dependencies:**

- **bundle install**

- **Set up the database:**
   
        rails db:create
        rails db:migrate

- **Running Tests**
- **Run RSpec tests to ensure the correct implementation of soft delete functionality(choose myapp/spec/models/item_spec.rb if needed)) :**

        bundle exec rspec


- **Usage**
- **Create a new Item:**
        item = Item.create(name: "Example Item")

- **Soft delete an item:**
        item.soft_delete

- **Restore a soft-deleted item:**
        item.restore

- **Query items (soft-deleted items are excluded by default):**
        all_items = Item.all











