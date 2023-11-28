# Interview-Bot-Client
Interview bot with improved framework for question difficulty estimation to ensure fair interviews.
## Setup and Usage

### Prerequisites

- [Python](https://www.python.org/) installed
- [virtualenv](https://pypi.org/project/virtualenv/) installed
- [FastAPI](https://fastapi.tiangolo.com/) and [Uvicorn](https://www.uvicorn.org/) installed (`pip install fastapi uvicorn`)
- [Postman](https://www.postman.com/) for testing API requests

### Getting Started

1. Clone the repository:

    ```bash
    git clone https://github.com/Pritish-Sinha/Interview-Bot-Client.git
    ```

2. Navigate to the project directory:

    ```bash
    cd chatgpt-interviewer-bot-backend
    ```

3. Create a virtual environment:

    ```bash
    python -m venv venv
    ```

4. Activate the virtual environment:

    - **On Windows:**

        ```bash
        .\venv\Scripts\activate
        ```

    - **On macOS/Linux:**

        ```bash
        source venv/bin/activate
        ```

5. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

6. Set environment variables:

    Create a `.env` file in the project root and add the following:

    ```env
    OPEN_AI_KEY=your_openai_api_key
    OPEN_AI_ORG=your_openai_organization_id
    ELEVENLABS_KEY=your_elevenlabs_api_key
    ```

    Replace `your_openai_api_key`, `your_openai_organization_id`, and `your_elevenlabs_api_key` with your respective API keys.

7. Run the server:

    ```bash
    uvicorn main:app --reload
    ```

    The server will start on `http://127.0.0.1:8000`.

### Testing with Postman

1. Open Postman.

2. Use the following endpoint to transcribe and get a chat response:

    - **Method:** POST
    - **URL:** `http://localhost:8000/talk`
    - **Body:** Select `form-data` and add a key `file` with the value being an audio file.

3. To clear chat history:

    - **Method:** GET
    - **URL:** `http://localhost:8000/clear`

### Contributors

- Pritish Sinha ([GitHub](https://github.com/your-username))

Feel free to contribute or open issues!