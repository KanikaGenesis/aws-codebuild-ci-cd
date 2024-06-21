# AWS CodeBuild CI/CD Project

This project demonstrates how to use AWS CodeBuild to automate the process of building and packaging a web application. By integrating various AWS services, it ensures a seamless and efficient CI/CD pipeline.

## Steps to Create the Deployment

To create a deployment, I set up the following resources in AWS:

1. **AWS CodeCommit**
   - Used as the source of the project’s code/files.

2. **EC2 Instance**
   - Selected Amazon Linux 2 and Java Coretto 8 as the runtime environment.

3. **S3 Bucket**
   - Created to store build artifacts produced during the build process.

4. **Buildspec.yml File**
   - Configured with the following phases:
     - **Install**: Install dependencies (e.g., Java Coretto 8).
     - **Pre_build**: Retrieve an access token to our CodeArtifact repository.
     - **Build**: Build the web app project.
     - **Post_build**: Package the machine code using the settings in the `settings.xml` file.

5. **IAM Role**
   - Edited to include necessary permissions for accessing CodeArtifact dependencies and managing build processes.

6. **CloudWatch Logs**
   - Enabled to keep records of all build processes.

## Key Learnings

- **AWS CodeBuild Integration**: The integration of AWS CodeBuild with other AWS services significantly streamlined the CI/CD pipeline, reducing manual overhead.
- **IAM Role Configuration**: Properly configuring IAM roles and policies is crucial for ensuring the right permissions are in place for each service.
- **Artifact Management**: Using S3 buckets for storing build artifacts ensures that all resources needed for running the application are bundled and accessible.

## Conclusion

This project highlights the efficiency and reliability of using AWS CodeBuild for automating the build and packaging processes in a CI/CD pipeline. The setup ensures minimal downtime, reduces manual errors, and provides a scalable solution for application deployment.

## Author

Kanika Mathur

[GitHub](https://github.com/KanikaGenesis) | [LinkedIn](https://linkedin.com/in/kanika-mathur-083080121/)
