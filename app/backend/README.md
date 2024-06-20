# Backend Directory Overview

The `app/backend` directory contains the server-side code for the application. It is built using [Quart](https://quart.palletsprojects.com/), a Python framework for asynchronous web applications. The server-side code communicates with the frontend using the [AI Chat HTTP Protocol](https://aka.ms/chatprotocol).

The main entry point for the backend is the `app.py` file. This file sets up the application, configures routes, and initializes various services such as Azure Cognitive Services, Azure Search, and OpenAI.

The `app.py` file imports various configurations, decorators, and utility functions from other files in the `app/backend` directory. It also sets up the Azure Monitor for OpenTelemetry to collect telemetry data.

The backend supports various features such as user authentication, document processing, search, and chat. These features are implemented in various modules in the `app/backend` directory.

The backend also integrates with Azure AI Search for indexing and retrieval of documents, and optionally with GPT-4 for reasoning over image-heavy documents.

The backend is deployed as an Azure App Service, as configured in the `infra/main.bicep` file. The deployment configuration includes settings for the Python runtime, managed identity, virtual network, and other Azure resources.

For more detailed information about customizing the backend, refer to the [Customizing the backend](docs/customization.md#customizing-the-backend) section in the `docs/customization.md` file.