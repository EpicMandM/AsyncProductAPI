# Readme

This code is a simple .Net application that implements three endpoints for an API that receives requests to add a listing, check the status of the listing, and retrieve the final status of the listing.

## Dependencies

This application depends on the following packages:

- Microsoft.EntityFrameworkCore

### Endpoints

The application has three endpoints:

- `api/v1/products` : accepts a `ListingRequest` object, updates its status, and saves it to the database. Returns a `Results.Accepted` object that provides a URL to check the status of the request.
- `api/v1/productstatus/{requestId}` : accepts a `requestId` and returns the status of the request. If the request is complete, it returns a `Results.Redirect` object to the URL of the final result.
- `api/v1/products/{requestId}` : accepts a `requestId` and returns the final result of the request.
