# AI Researcher Example

**These instructions assume you are in the `ai-researcher/` directory**

## Running the Agent

First, install the dependencies:

```sh
cd agent
poetry install
```

# AI Researcher Example

## Project Motivation and Features

The AI Researcher project aims to provide a robust platform for conducting complex research queries using AI. The project is divided into two main components: the `agent` and the `ui`. The `agent` handles the backend processing and research logic, while the `ui` provides a user-friendly interface for interacting with the research agent.

### Key Features

- **Agent**: Utilizes advanced AI models to break down complex queries into manageable steps, perform searches, and summarize results.
- **UI**: A Next.js-based frontend that allows users to input queries, view progress, and see summarized results.
- **CopilotKit Integration**: Streams the graph state from the backend to the frontend, providing real-time updates on the research process.
- **LangGraph**: Defines the workflow graph and the entry point for the agent, ensuring a structured and efficient research process.

## Functionalities

### Agent

The `agent` folder contains the core logic for processing research queries. It uses the following components:

- **Steps Node**: Breaks down the user's query into smaller steps.
- **Search Node**: Performs web searches based on the steps.
- **Summarize Node**: Summarizes the final results, including all relevant information and reference links.
- **Extract Node**: Extracts information from search results.

The agent is configured using `langgraph` and `copilotkit` to manage the workflow and state.

### UI

The `ui` folder contains the frontend code, built with Next.js. It provides the following functionalities:

- **Home View**: Allows users to input their research queries.
- **Results View**: Displays the progress and final results of the research.
- **Real-time Updates**: Uses CopilotKit to stream the graph state from the backend, providing real-time updates on the research process.

## CopilotKit Integration

The project uses CopilotKit to stream the graph state from the backend to the frontend. This allows for real-time updates on the research process, providing users with immediate feedback on the progress and results of their queries.

## Graph Agent

The graph agent is defined using `langgraph` and consists of multiple nodes that handle different parts of the research process. The workflow is structured to ensure that each step is executed in sequence, with the results being summarized and presented to the user in a clear and concise manner.

## Setup Instructions

### Running the Agent

First, install the dependencies:

```sh
cd agent
poetry install
```

Then, create a `.env` file inside `./agent` with the following:

```
OPENAI_API_KEY=...
TAVILY_API_KEY=...
```

IMPORTANT:
Make sure the OpenAI API Key you provide, supports gpt-4o.

Then, run the demo:

```sh
poetry run demo
```

## Running the UI

First, install the dependencies:

```sh
cd ./ui
pnpm i
```

Then, create a `.env` file inside `./ui` with the following:

```
OPENAI_API_KEY=...
```

Then, run the Next.js project:

```sh
pnpm run dev
```

## Usage

Navigate to [http://localhost:3000](http://localhost:3000).

# LangGraph Studio

Run LangGraph studio, then load the `./agent` folder into it.

Make sure to create the `.env` mentioned above first!
