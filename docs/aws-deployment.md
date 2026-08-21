# AWS Deployment Notes

## Amazon S3

The Angular application is built into deployable static assets. Amazon S3 can host those assets as a static website or as the origin for a more complete AWS delivery architecture.

A production deployment should use appropriate bucket permissions and should not expose unrelated data or credentials through the bucket.

## AWS Lambda

AWS Lambda provides a serverless execution model for backend functionality. In this project, Lambda is part of the cloud/serverless concepts explored during the course. A production implementation should define clear function responsibilities, configure environment variables securely, and apply least-privilege IAM permissions.

## CORS

Because a browser-based frontend and API can be hosted at different origins, CORS configuration is required for approved cross-origin requests. CORS should be restricted to known application origins rather than allowing unrestricted access in a production environment.

## Deployment Checklist

- Build the Angular application successfully.
- Confirm the production configuration points to the correct API endpoint.
- Upload only intended frontend artifacts to S3.
- Configure the required S3 hosting/access behavior.
- Configure API/serverless components.
- Configure CORS for the expected frontend origin.
- Verify API requests from the deployed frontend.
- Confirm no credentials or secrets are present in the repository or frontend bundle.
- Test the application after deployment.

## Security Note

AWS access keys, passwords, database credentials, tokens, and private environment files must not be committed to GitHub. Use environment variables, AWS IAM, Secrets Manager, or another approved secret-management approach instead.
