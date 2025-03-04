\# ai-assistant

###Project Structure
```
ai-chat-app/
│── backend/
│   │── app.py
│   │── requirements.txt
│   │── .env
│   │── venv/ (virtual environment, not committed to Git)
│   ├── static/
│   │   ├── js/
│   │   │   ├── chat.js
│   │   ├── css/
│   │   │   ├── styles.css
│   ├── templates/
│   │   ├── index.html
│   ├── README.md
│── frontend/
│   │── index.html
│   │── assets/
│   │   ├── css/
│   │   │   ├── styles.css
│   │   ├── js/
│   │   │   ├── app.js
│── README.md
```
### Project Documentation

#### AI Chat Web App

This is a simple AI-powered web chat application using HTML, CSS, JavaScript, Bootstrap, Python Flask, and OpenAI's GPT-4o. The frontend provides an interactive chat experience, while the backend handles AI responses via OpenAI's API.

---

#### **Features**
- A sidebar navigation for different AI assistants:
  - **Essay Writer**
  - **Story Teller**
  - **Math Solver**
  - **Email Writer**
  - **Translator**
  - **Code Generator**
- Chat Interface:
  - User messages appear on the right.
  - AI responses appear on the left.
  - Suggested prompts for each assistant.

---

#### **Installation Guide**

#### **Backend Setup**
1. Install Python (≥3.8) if not installed.
2. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/ai-chat-app.git
   cd ai-chat-app/backend



#### Create and activate a virtual environment:
##### On Windows:
```
python -m venv venv
venv\Scripts\activate
```
##### On Mac/Linux:
```
python3 -m venv venv
source venv/bin/activate
```
#### Install dependencies:
```
pip install -r requirements.txt
```
#### Set up .env file with OpenAI API key:
```
OPENAI_API_KEY=your-api-key
```
#### Run the Flask server:
```
python app.py
```

#### Frontend Setup
No installation required. Just open index.html in a browser.

### How It Works
1. User selects an AI assistant from the sidebar.
2. Suggested prompts appear.
3. User enters a prompt.
4. The request is sent to the Flask backend.
5. The AI (GPT-4o) responds, and the response is displayed in the chat.

### File Structure
`backend/` contains the Flask backend.
`frontend/` holds the HTML, CSS, and JS files for the UI.
`README.md` contains setup and usage instructions.

### API Endpoint

POST `/api/chat`
- Request:
```
{
  "assistant_type": "Essay",
  "user_message": "Write an essay on climate change"
}
```
- Response:
```
{
  "response": "Climate change is a pressing issue..."
}
```

### Future Improvements
- User authentication.
- Save chat history.
- Dark mode toggle.