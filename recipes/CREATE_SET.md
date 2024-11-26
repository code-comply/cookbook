# Creating a drawing set

Table of Contents:

- [Prerequisites](#prerequisites)
- [Steps](#steps)

## Prerequisites:

- ID of the organization that will own the drawing set
- ID of the user that will own the drawing set
- [ID of the project that will include the drawing set](CREATE_PROJECT.md)
- [The request needs to be authenticated](AUTHENTICATION.md)

## Steps

1. Create a drawing set

    Method: POST
   URL: https://api-dev.codecomply.com/api/v1/set

    Request Body:
    ```json
    {
        "name": "Default set",
        "project_id": "<PROJECT_ID>",
        "user_id": "<USER_ID>", 
        "organization_id": "<ORGANIZATION_ID>"
    }
    ```
