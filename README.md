# Negotiation Skills Feedback System

## 1. Overview

The Negotiation Skills Feedback System is a web application designed to help individuals improve their negotiation skills through interactive chat simulations and detailed feedback. The application leverages a backend API to manage chat sessions, retrieve feedback, and store chat histories. The frontend is built using Streamlit, providing a user-friendly interface for creating sessions, chatting with an AI assistant, and viewing detailed feedback and evaluation metrics.

## 2. Features

1. **Create New Sessions**: Users can create new negotiation sessions by providing a session name, selecting a job role, and entering a prompt.
2. **Interactive Chat**: Engage in real-time negotiation simulations with an AI assistant. The chat history is saved for each session.
3. **Session Feedback**: Receive detailed feedback on your negotiation performance, including scores and reasoning for each evaluation metric.
4. **Evaluation Metrics**: Visualize your performance through radar charts and individual metric breakdowns.
5. **Suggestions for Improvement**: Get actionable suggestions to enhance your negotiation skills.
6. **Chat Log**: Review the complete chat history for each session.
   
## 3. How it Works

### 3.1 Leveraging LLMs for Chat and Feedback

The core functionality of this application relies on Large Language Models (LLMs) to provide an interactive and insightful experience:

1. **Interactive Chat Sessions**: When a new session is created, users can engage in a chat with an AI assistant powered by an LLM. The conversation is driven by carefully crafted prompts to simulate real-world negotiation scenarios. This allows users to practice their negotiation skills in a controlled environment.
2. **Feedback Generation**: Once a session has ended, the LLM is employed again to analyze the entire conversation. By using specialized prompts, the system generates detailed feedback on the user's performance. This includes scoring various metrics, providing reasoning behind each score, and offering suggestions for improvement. The feedback is designed to be comprehensive and actionable, helping users to identify their strengths and areas that need enhancement


### 3.2 The Role of Prompt Engineering

Prompt engineering is a critical component in making effective use of LLMs. By designing specific prompts, the application ensures that the LLM can provide meaningful and contextually relevant responses during the chat sessions and produce detailed feedback after the sessions. This involves:

1. **Designing Chat Prompts**: Crafting prompts that guide the LLM to respond appropriately during negotiations, simulating realistic scenarios and challenges that users might face.
2. **Generating Feedback Prompts**: Creating prompts that instruct the LLM to analyze the conversation and generate structured feedback, including scores and suggestions for improvement.

## 4. Technologies Used

- **Frontend**: Streamlit, Plotly
- **Backend**: Flask, SQLAlchemy
- **Database**: SQLite (or any other SQL database supported by SQLAlchemy)
- **APIs**: RESTful APIs for managing sessions, retrieving chat histories, and feedback
- **LLMs**: Used for chat simulations and feedback generation through prompt engineering

## 5. Installation

1. **Clone the Repository**:
   
    git clone https://github.com/yourusername/negotiation-skills-feedback.git
    cd negotiation-skills-feedback
   
2. **Set Up the Backend**:
    
    cd backend
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install -r requirements.txt
    flask run
    
3. **Set Up the Frontend**:
   
    cd frontend
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install -r requirements.txt
    streamlit run app.py   

## 6. Usage

1. **Start the Backend**:    
    cd backend
    flask run

2. **Start the Frontend**:
    cd frontend
    streamlit run app.py
    
3. **Access the Application**:
    Open your web browser and navigate to `http://localhost:8501` to use the Negotiation Skills Feedback System.

## 7. API Endpoints

### 7.1 Sessions
- **GET /chat_logs**: Retrieve all completed chat sessions.
- **POST /session**: Create a new session with a given name, job role, and prompt.

### 7.2 Session Results
- **GET /session/<session_id>/result**: Retrieve feedback and score for a specific session.
- **GET /session/<session_id>/history**: Retrieve chat history for a specific session.

### 7.3 Messages
- **POST /session/<session_id>/message**: Send a message to the AI assistant in a specific session and receive a response.

## 8. Contributing

Contributions are welcome! Please open an issue or submit a pull request for any bugs, feature requests, or improvements.
