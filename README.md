# AsyncProductAPI

This is a .NET Web API that allows users to request product listings and check the status of their requests. The API is built using the following technologies:

- C# programming language
- .NET 6 Web API framework
- Entity Framework Core for data persistence
- SQLite as the database engine

## Getting Started

To run this API on your local machine, you will need to have the following installed:

- .NET 6 SDK
- Visual Studio Code or Visual Studio IDE

Once you have these installed, you can follow these steps to run the API:

1. Clone the repository to your local machine.
2. Open the solution in Visual Studio Code or Visual Studio.
3. Run the application.

## Usage

### POST /api/v1/products

This endpoint allows users to request product listings. Users can make a POST request to this endpoint with a JSON body that contains the details of the listing request. The API will respond with a 202 Accepted status code and a location header that contains the URL to check the status of the request.

### GET /api/v1/productstatus/{requestId}

This endpoint allows users to check the status of their product listing request. Users can make a GET request to this endpoint with the request ID of their listing. The API will respond with a JSON object that contains the status of the request.

### GET /api/v1/products/{requestId}

This endpoint allows users to retrieve the final result of their product listing request. Users can make a GET request to this endpoint with the request ID of their listing. The API will respond with the final result of the listing request.

## Configuration

The API is configured to use SQLite as its database engine. The connection string for the database is set in the `AppDbContext` class, which is located in the `AsyncProductAPI.Data` namespace. The database file is stored in the root directory of the application and is named `RequestDB.db`.
