# Creating a drawing set

Table of Contents:

- [Prerequisites](#prerequisites)
- [Steps](#steps)

## Prerequisites:

- [ID of the project that will include the drawing set](CREATE_PROJECT.md)
- [The request needs to be authenticated](AUTHENTICATION.md)

## Steps

1. Create a drawing set

    Method: POST
   URL: https://api-dev.codecomply.ai/api/v1/set

    Request Body:
    ```json
    {
        "name": "Default set",
        "project_id": "<PROJECT_ID>"
    }
    ```
