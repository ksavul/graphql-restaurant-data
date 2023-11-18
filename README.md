# README

## Project Title

A GraphQL API for Restaurant Management

## Description

This project provides a GraphQL API for managing restaurant data. It allows users to query information about restaurants, including their menus, and perform CRUD (Create, Read, Update, Delete) operations on restaurant data. The application is built using Node.js and GraphQL.

## Features

- **Query Operations**: Retrieve single restaurant information or a list of all restaurants.
- **Create Operation**: Add new restaurants to the database.
- **Update Operation**: Modify existing restaurant details.
- **Delete Operation**: Remove restaurants from the database.

## Installation

1. Clone the repository:
   ```bash
   git clone [repository-link]
   ```
2. Navigate to the project directory:
   ```bash
   cd [project-directory]
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the server:
   ```bash
   npm start
   ```

## Usage

After starting the server, navigate to `http://localhost:5500/graphql` to access the GraphiQL interface where you can execute GraphQL queries and mutations.

### Example Queries and Mutations

- Query a single restaurant:
  ```graphql
  {
    restaurant(id: 1) {
      name
      description
      dishes {
        name
        price
      }
    }
  }
  ```

- Query all restaurants:
  ```graphql
  {
    restaurants {
      name
      description
      dishes {
        name
        price
      }
    }
  }
  ```

- Add a new restaurant:
  ```graphql
  mutation {
    setrestaurant(input: { name: "New Restaurant", description: "New Description" }) {
      name
    }
  }
  ```

- Delete a restaurant:
  ```graphql
  mutation {
    deleterestaurant(id: 1) {
      ok
    }
  }
  ```

## Contributing

Contributions to enhance the functionality and efficiency of this GraphQL API are welcome. Please follow the standard fork-and-pull request workflow.

## License

This project is licensed under the terms of the MIT license. For more details, refer to the LICENSE file in the repository.
