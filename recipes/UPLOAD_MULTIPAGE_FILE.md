# Uploading a multipage file

Table of Contents:

- [Prerequisites](#prerequisites)
- [Steps](#steps)
  
## Prerequisites:

- ID of the organization that will own the plans
- ID of the user that will own the plans
- ID of the project that will include the plans
- ID of the drawing set that will include the plans
- [The request needs to be authenticated](AUTHENTICATION.md)

## Steps

1. Create an upload file

    Method: POST
    URL: https://api-dev.codecomply.com/api/v1/upload_file

    Request Body:
    ```json
    {
        "name": "My set of plans",
        "active": false,
        "project_id": "<PROJECT_ID>",
        "set_id": "<SET_ID>",
        "organization_id": "<ORGANIZATION_ID>",
        "user_id": "<USER_ID>",
        "original_mime": "<the MIME of the file, usually application/pdf>"
    }
    ```

    The request above return the upload file entity including a URL, under the "original_signed" key.

2. Upload the file

    Method: PUT
    URL: `original_signed` from the previous step

    Request Body: the binary of the file to be uploaded

3. Activate the upload file

    Method: PUT
    URL: https://api-dev.codecomply.com/api/v1/upload_file/<UPLOAD_FILE_ID>

    Request Body:
    ```json
    {
        "active": true
    }
    ```
