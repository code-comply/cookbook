# Creating a project

Table of Contents:

- [Prerequisites](#prerequisites)
- [Steps](#steps)

## Prerequisites:

- ID of the organization that will own the project
- ID of the user that will own the project
- [The request needs to be authenticated](AUTHENTICATION.md)

## Steps

1. Create a project

    Method: POST
    URL: https://api-dev.codecomply.com/api/v1/project

    Request Body:
    ```json
    {
        "name": "My Project",
        "pid": "00000",
        "active": true,
        "organization_id": "<ORGANIZATION_ID>",
        "user_id": "<USER_ID>",
        "metadata": {
            "state": {
                "id": "fl",
                "name": "Florida"
            },
            "applicable_codes": []
        },
        "is_active": true
    }
    ```

