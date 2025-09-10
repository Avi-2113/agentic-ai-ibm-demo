# agentic-ai-ibm-demo

🚀 Agentic AI on IBM Cloud (Watsonx.ai)

This repo demonstrates how to build and deploy an Agentic AI using IBM Cloud Watsonx.ai.
It follows the steps from the guide Demo on Agentic AI on IBM Cloud.pdf.

📌 Features

Create AI Agent using Watsonx.ai

Use Mistral-large model (or other foundation models)

Deploy agent to IBM Cloud Deployment Space

Interact with the agent via Web Preview or API

⚙️ Setup Instructions
1. IBM Cloud Setup

Go to IBM Cloud
 → Login

From the navigation menu → Watsonx.ai → AI Agents

Create a new Project (Free Plan)

Associate Watsonx.ai Runtime Service with your project

2. Create API Key

IBM Cloud Dashboard → Manage → Access (IAM)

Go to API Keys → Click Create

Copy & save the generated API key (you’ll need it later)

3. Deploy Your Agent

Create a Deployment Space → Select Watsonx.ai Runtime

Deploy your agent into the space

Once deployed → click Preview to test the agent

💻 Using the API

You can call your deployed agent via REST API.

Example (Python):

import requests

API_KEY = "your-api-key-here"
URL = "https://<your-region>.watsonx.ai.cloud.ibm.com/v1/agents/<agent-id>/message"

headers = {
    "Content-Type": "application/json",
    "Authorization": f"Bearer {API_KEY}"
}

data = {
    "input": {
        "text": "Hello Agent, what can you do?"
    }
}

response = requests.post(URL, headers=headers, json=data)
print(response.json())

📂 Repository Structure
agentic-ai-ibm-demo/
│── Demo on Agentic AI on IBM Cloud.pdf   # Step-by-step setup guide
│── call_agent.py                         # Sample Python script to call the agent
│── README.md                             # Project documentation

🙌 Contributing

Feel free to fork this repo and extend it with:

Node.js / React frontend

Automation examples

Advanced agent configurations

📜 License

This project is released under the MIT License.
