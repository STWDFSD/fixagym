# AI Chatbot API

A simple AI chatbot API built with FastAPI and OpenAI's GPT model.

## Setup

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Create a `.env` file in the root directory with the following content:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   MODEL_NAME=gpt-3.5-turbo
   ```
   Replace `your_openai_api_key_here` with your actual OpenAI API key.

## Running the Application

Start the server with:
```bash
uvicorn main:app --reload
```

The API will be available at `http://localhost:8000`

## API Endpoints

### POST /chat
Send a chat message to the AI.

Request body:
```json
{
    "messages": [
        {
            "role": "user",
            "content": "Hello, how are you?"
        }
    ]
}
```

Response:
```json
{
    "response": "I'm doing well, thank you for asking! How can I help you today?"
}
```

### GET /
Returns a welcome message.

## API Documentation

Once the server is running, you can access the interactive API documentation at:
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`