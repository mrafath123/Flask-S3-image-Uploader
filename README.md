# Flask S3 Image Upload

This is a simple Flask web application for uploading images to Amazon S3 (Simple Storage Service). Uploaded images are stored in an S3 bucket and can be accessed via signed URLs.

## Setup

1. Clone this repository to your local machine.
2. Install the required dependencies using pip:
    ```
    pip install flask boto3
    ```
3. Configure your AWS credentials in the `image.py` file:
    ```python
    AWS_ACCESS_KEY_ID = 'Your access key'
    AWS_SECRET_ACCESS_KEY = 'Your secret key'
    AWS_REGION = 'us-east-1'
    S3_BUCKET = 'Your bucket name'
    ```
4. Run the Flask application:
    ```
    python image.py
    ```
5. Access the application in your web browser at `http://localhost:5000`.

## Usage

1. Open the web application in your browser.
2. Click on the "Choose File" button to select an image file for upload.
3. Click the "Upload" button to upload the selected image.
4. Once the upload is complete, the uploaded image will be displayed on the page along with a signed URL for direct access to the image.

## Notes

- Ensure that your AWS credentials have the necessary permissions to upload files to the specified S3 bucket.
- Adjust the expiration time for signed URLs (`ExpiresIn` parameter in `generate_presigned_url` function) as needed.
- This application does not include error handling for AWS S3 operations. You may want to enhance it for production use.

