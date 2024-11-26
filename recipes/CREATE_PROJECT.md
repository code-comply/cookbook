# Creating a project

Table of Contents:

- [Prerequisites](#prerequisites)
- [Steps](#steps)

## Prerequisites:

- [The request needs to be authenticated](AUTHENTICATION.md)

## Steps

1. Create a project

    Method: POST
    URL: https://api-dev.codecomply.ai/api/v1/project

    Request Body:
    ```json
    {
        "name": "My Project",
        "pid": "00000",
        "active": true,
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

