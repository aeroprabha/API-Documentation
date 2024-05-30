# MeeraAI API

## Getting Started

Welcome to the Meera Chatbot API Documentation. This API enables programmatic interaction with the Meera Chatbot platform, facilitating the integration of chatbot capabilities into your applications. This document provides comprehensive information on the endpoints available, authentication requirements, error handling, and usage examples.

## Base URL

The base URL for all API endpoints is:

**API Endpoint**: `https://chatbot.meera.ai`

## Authorization

### Basic Auth

For all API requests, users need to use Basic Authentication with the API token generated from the Login API. Set the header `Authorization: {X-Token-Auth}` and ensure the `Content-Type` and `Accept` headers are set to `application/json`.

## Errors

Meera AI uses conventional HTTP response codes to indicate the success or failure of an API request. In general:

- Codes in the 2xx range indicate success.
- Codes in the 4xx range indicate an error due to the information provided (e.g., a required parameter was omitted, authentication failed, etc.).
- Codes in the 5xx range indicate an error with Meera AI's servers (these are rare).

## Authorization

### Basic Auth

# API Endpoint: Login

## Login

Logs in users and retrieves an authentication token. This endpoint allows the users to authenticate by providing their email and password. Upon successful authentication, a token is returned which can be used for accessing other protected resources.

### Error Codes

| Error Code | Description               |
|------------|---------------------------|
| 200        | Success                   |
| 400        | Wrong credentials response|

### Authorization

**Basic Auth**

This folder is using Basic Auth from the MeeraAI API collection.

## POST

### Login User and Get Token

**Endpoint**: `//api/v1/login`

Provide user email and password as a JSON request.

**Required:**
- Email
- Password

### Authorization

**Basic Auth**

This request uses Basic Auth from the MeeraAI API collection.

### Headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

### Body

```json
{
  "email": "<email>",
  "password": "<string>"
}
