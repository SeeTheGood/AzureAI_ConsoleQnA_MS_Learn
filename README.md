Overview

qna_app is a console application that interacts with Azure's AI Language Question Answering service. It allows users to input questions and receive answers based on a predefined knowledge base. The application leverages Azure's AI capabilities to provide accurate and relevant answers to user queries.

Prerequisites

Before running the application, ensure you have the following:

Azure Subscription: An active Azure subscription with access to the AI Language Question Answering service.
Azure AI Language Question Answering Resource: Set up the Question Answering resource in the Azure portal. Note down the endpoint URL and key.
.NET SDK: .NET SDK installed on your machine. You can download it from the official .NET website.
Configuration

The application requires configuration settings to connect to Azure services. These settings should be placed in an appsettings.json file in the root directory of your project.
The file should have the following structure:
{
  "AIServicesEndpoint": "<Your_Azure_Endpoint>",
  "AIServicesKey": "<Your_Azure_Key>",
  "QAProjectName": "<Your_Project_Name>",
  "QADeploymentName": "<Your_Deployment_Name>"
}
Replace the placeholders with your actual Azure endpoint, key, project name, and deployment name.

Usage

Building the Application
Clone the repository: Clone the repository to your local machine.
Navigate to the project directory: Open a terminal or command prompt and navigate to the directory containing the qna_app project.
Build the project: Run the following command to build the project: dotnet build
Running the Application
Run the application: Execute the following command to run the application:dotnet run

Ask Questions: The application will prompt you to input questions. Type your question and press Enter to receive an answer.
Exit the application: Type quit and press Enter to exit the application.

Code Structure

Namespaces: The application uses namespaces to organize code and handle dependencies.
Configuration: The IConfigurationBuilder reads configuration settings from the appsettings.json file.
Client Initialization: The QuestionAnsweringClient is created using the Azure endpoint and key.
Question Submission: The application prompts the user for questions, submits them to the Azure service, and displays the answers along with confidence levels and sources.
Error Handling: The application includes basic error handling to catch and display exceptions.
Dependencies

The application relies on the following NuGet packages:

Azure.AI.Language.QuestionAnswering
Azure.Core
Microsoft.Extensions.Configuration
Microsoft.Extensions.Configuration.Json
These dependencies are specified in the project's .csproj file and are automatically restored when you build the project.
