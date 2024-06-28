# GraphQL Web Services

Welcome to GraphQL Web Services! This README will guide you through setting up, running, and contributing to the application.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Contact](#contact)

## Overview

GraphQL Web Services is web services that use ChilliCream GraphQL platform for describing your data and then querying it that gives the client control over exactly what they need.

## Features

- Hot Chocolate "enables you to create GraphQL services for .NET"
- Strawberry Shake "enables you to create GraphQL clients for.NET"
- Banana Cake Pop "enables you to run queries and explore a GraphQL endpoint using a Monaco-based GraphQL IDE"
- Green Donut "enables better performance when loading data"

## Prerequisites

- [.Net] (version 8.0.0)
- [VS 2022]

## Installation

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/abdooAhmed/WebService-Using-GraphQL.git
   ```

## Usage

1. Running Locally :

   1. Start the Northwind.GraphQL.Service project without debugging "Click right on Northwind.GraphQL.Service project Debug -> Start without Debuging"
   2. Navigate to `https://localhost:5121/graphql` to open BananaCakePop user interface
   3. Click the Schema Definition tab, and note the query and type definitions for Category and Product
   4. Start the Northwind.WebApi.Client.Mvc project without debugging so that we can send messages to the RabbitMQ queue
   5. Test one if the following queries to make sure that this web services working well

      ```
         query AllCategories {
            categories {
            categoryId
            categoryName
            description
            }
         }

      ```

      ```
      query Condiments {
            category (categoryId: 2) {
            categoryId
            categoryName
               products {
               productId
               productName
               unitPrice
               }
            }
         }
      ```

      ```
      query BeverageProducts {
         productsInCategory (categoryId: 1) {
         productId
         productName
         unitsInStock
         }
      }

      ```

   6. Start the Northwind.GraphQL.Client.Mvc project without debugging and Enter another category ID that exists, for example, 4

## Contact

-If you have any questions or feedback, please reach out to me at [abdulrahman.ahmed.abdulah@gmail.com].
