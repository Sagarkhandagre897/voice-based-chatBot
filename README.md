# voice-based-chatBot
live demo -- https://voice-based-chatbot.onrender.com/

This project is a Voice-based AI Chatbot that allows users to interact with an AI-powered virtual assistant using their voice. The chatbot leverages the capabilities of the OpenAI GPT-3 API to process natural language queries and provide relevant responses. The application is implemented using a combination of front-end technologies (HTML, CSS, JavaScript) for the user interface and a Node.js server for handling API requests and interactions with the GPT-3 API.

Project Flow:

Front-end Interface: The HTML page provides a simple and intuitive user interface where users can see the chatbot's responses and interact by speaking their queries.

Voice Input Processing: The client-side JavaScript utilizes the Web Speech API (SpeechRecognition) to capture the user's voice input. As the user speaks, the voice input is transcribed and displayed on the screen.

Rate Limiting (Client-side): To avoid sending API requests too frequently, client-side rate-limiting is implemented using the lodash.debounce function. It ensures that only one API request is sent after a brief pause in the user's speech.

API Request Handling (Server-side): When the user's voice input is processed, the client sends an API request to the Node.js server via a POST request. The server-side uses express-rate-limit middleware to enforce rate-limiting on API requests, limiting the number of requests per minute.

OpenAI GPT-3 API Interaction: The server communicates with the OpenAI GPT-3 API using the openai Node.js library. It sends the voice input to the API for processing and receives the AI-generated response.

Response Display: The GPT-3 response is sent back to the client and displayed on the HTML page, showing the chatbot's reply to the user's query.

Voice Output: The chatbot's response is also spoken aloud using the Web Speech API (SpeechSynthesis). The response is played back to the user as an audio message.
