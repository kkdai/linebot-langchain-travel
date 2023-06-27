# Langchain LINE Bot

This project is an implementation of a LINE Bot using FastAPI, OpenAI's GPT-3.5 model and multiple tools for different functions like weather data, travel POIs, tickets, experiences, and product data.

## Features

- Automated text responses using OpenAI's GPT-3.5 model.
- Integrated with various tools including:
  - TravelPOITool: to provide point of interest information for travel related queries.
  - TravelTicketTool: to provide ticket information for travel related queries.
  - TravelExpTool: to provide travel experience related data.
  - WeatherDataTool: to provide weather data.
  - ProductTool: to provide product related data.
  - DuckDuckGoSearchRun: to provide search functionality using DuckDuckGo.

## Installation

To install the necessary dependencies for this project, use:

```sh
pip install fastapi aiohttp linebot python-dotenv
```

Additionally, you'll need to setup the environment variables `ChannelSecret` and `ChannelAccessToken` in a `.env` file at your project's root directory.

## Usage

Once you've cloned this repository and installed the necessary dependencies, you can run the FastAPI server with the command:

```sh
uvicorn main:app --reload
```

Replace `main` with the name of your Python file.

The bot will listen for POST requests on the `/callback` endpoint. It processes text messages sent by users, using OpenAI's GPT-3.5 model to generate responses if the incoming message starts with `:gpt`.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update the tests as appropriate.

## License

This project is licensed under the terms of the MIT license.
