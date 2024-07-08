# Introduction to Using WRFExpress for Running WRF on AWS

`WRFExpress` is designed to streamline the process of running Weather Research and Forecasting (WRF) models on AWS clusters. This tool simplifies complex configurations and automates various steps, making it accessible even to those without deep technical expertise. Here’s how you can utilize WRFExpress to get started with your WRF simulations.

## Website Interface

The web interface of WRFExpress allows you to easily define your simulation domain by selecting an area on an interactive map. Here’s a step-by-step guide on how to use it:

1. **Access the Website**: Navigate to the WRFExpress website and log in with your credentials.
2. **Select a Domain**: Use the interactive map to draw rectangles defining your simulation domains. You can create multiple nested domains by drawing new rectangles within existing ones.
3. **Configuration Settings**: On the right side of the screen, fill in the necessary configuration details:
   - **Orcid ID**: Enter your ORCID ID.
   - **API Token**: Provide your API token.
   - **Start Date and End Date**: Specify the start and end dates for your simulation period.
   - **Time Interval**: Set the time interval for data points (e.g., 6 hours).
   - **Geographical Data Resolution**: Enter the resolution for geographical data.
   - **DX and DY**: Specify the grid spacing for your simulation.
4. **Update Configuration**: After filling in the details, click on "Update Configuration" to save your settings.
5. **Generate Namelist**: Click on "Generate Namelist" to create the `namelist.wps` file, which is essential for running WRF.
6. **Generate Download Data Code**: Click on "Generate Download Data Code" to get the Python script for downloading necessary data files.

## Running WRF on AWS Cluster

After configuring your simulation domain and generating necessary files, follow these steps to run WRF on the AWS cluster:

1. **Upload Files**: Ensure that the `namelist.wps` file and any other required scripts are uploaded to the appropriate directories on the AWS cluster.
2. **Execute Scripts**: Use the provided Python script to run the necessary shell commands on the AWS cluster. This script will automate the execution of WRF-related tasks such as geogrid, ungrib, metgrid, and the WRF model itself.
3. **Monitor Progress**: The script includes features for monitoring job progress and displaying log files, making it easier to track the simulation’s status.

## Key Features of the Python Script

- **Shell Command Execution**: Automates the execution of multiple WRF-related shell scripts.
- **S3 Integration**: Uploads simulation outputs to an S3 bucket and generates a presigned URL for easy download.
- **Progress Monitoring**: Uses the `rich` library to display real-time progress of script execution and job queue status.
- **Error Handling**: Provides informative logs for troubleshooting any issues that arise during execution.

By following these steps, WRFExpress simplifies the setup and execution of WRF simulations on AWS, allowing users to focus more on their research and less on the technical complexities of the modeling process.
