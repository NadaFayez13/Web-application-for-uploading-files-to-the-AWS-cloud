# CLOUDY FILES

This project is a cloud-based web application that allows users to securely upload and access their files at any time. Once a file is uploaded through the user interface, it is automatically classified and stored in *Amazon S3*, with download links generated on the spot—making the process smooth, fast, and efficient.

The backend is built using Flask, and integrates with AWS services such as EC2 for 24/7 hosting, and S3 for scalable, secure storage. File handling and AWS operations are powered by the boto3 SDK, and the frontend is designed to support common file formats like PDF, JPG, PNG, and TXT.

