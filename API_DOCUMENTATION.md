# API Documentation for Scheme Eligibility System

## Overview
This document outlines the REST endpoints available in the Scheme Eligibility System and describes their usage.

## Base URL
```
http://api.example.com/v1
```

## Endpoints

### 1. Get Scheme Details
- **Endpoint:** `/schemes/{scheme_id}`
- **Method:** `GET`
- **Description:** Retrieves details of a specific scheme by its ID.
- **Parameters:**
  - `scheme_id` (path, required): The ID of the scheme to retrieve.
- **Response:**
  - `200 OK`: Scheme details in JSON format.

### 2. Check Eligibility
- **Endpoint:** `/eligibility/check`
- **Method:** `POST`
- **Description:** Checks eligibility for a specific scheme based on user input.
- **Request Body:** JSON object with user information and scheme ID.
- **Response:**
  - `200 OK`: Eligibility status.
  - `400 Bad Request`: If the request body is invalid.

### 3. List Available Schemes
- **Endpoint:** `/schemes`
- **Method:** `GET`
- **Description:** Retrieves a list of all available schemes.
- **Response:**
  - `200 OK`: Array of schemes in JSON format.

### 4. Create a New Scheme
- **Endpoint:** `/schemes`
- **Method:** `POST`
- **Description:** Creates a new scheme.
- **Request Body:** JSON object with scheme details.
- **Response:**
  - `201 Created`: The created scheme object.
  - `400 Bad Request`: If the request body is invalid.

### 5. Update an Existing Scheme
- **Endpoint:** `/schemes/{scheme_id}`
- **Method:** `PUT`
- **Description:** Updates the details of an existing scheme by its ID.
- **Parameters:**
  - `scheme_id` (path, required): The ID of the scheme to update.
- **Request Body:** JSON object with updated scheme details.
- **Response:**
  - `200 OK`: The updated scheme object.
  - `400 Bad Request`: If the request body is invalid.

### 6. Delete a Scheme
- **Endpoint:** `/schemes/{scheme_id}`
- **Method:** `DELETE`
- **Description:** Deletes a scheme by its ID.
- **Parameters:**
  - `scheme_id` (path, required): The ID of the scheme to delete.
- **Response:**
  - `204 No Content`: If the scheme was successfully deleted.
  - `404 Not Found`: If the scheme does not exist.

## Authentication
All endpoints require authentication. Please include a valid API token in the request headers.

## Conclusion
This documentation provides an overview of the REST endpoints for the Scheme Eligibility System. For further details or assistance, please refer to the developer documentation.
