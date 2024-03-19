# Assignment 2: DOG API

## Endpoints and Test Scenarios

### List all breeds

- **Verify that the status code is 200 (OK) when a valid endpoint is triggered**
- **Verify if the response time is within acceptable limits**
- **Verify that the response format is JSON**
- **Verify that the response body contains “message” and “status” fields**
- **Verify that the response body contains message fields with the list of all dog breeds and sub-breeds for a successful request**
- **Verify that the response body contains status fields as "success" for a successful request**
- **Verify that the breed names are valid (no spelling mistakes and special characters)**
- **Verify that there are no duplicate breeds**
- **Verify that the status code is 401 (Unauthorized) when proper authentication is not given**

### By Breed

- **Verify that the status code is 200 (OK) for a valid breed**
- **Verify if the response time is within acceptable limits**
- **Verify that the response format is JSON**
- **Verify that the response body contains “message” and “status” fields**
- **Verify that the "message" field contains a list of image URLs for the specified valid breed**
- **Verify that the response body contains status as "success" for a valid breed**
- **Verify that the images returned for the specified breed are valid and accessible**
- **Verify that the images belong to the correct breed**
- **Verify that the status code is 404 (Not Found) for an invalid breed**
- **Verify that the response body contains status as "error" for an invalid breed**
- **Verify that the response body contains message "Breed not found (master breed does not exist)" for an invalid/non-existing master breed**
- **Verify that the response body contains message "Breed not found (master breed does not exist)" for a sub-breed**
- **Verify that the status code is 401 (Unauthorized) when proper authentication is not given**
