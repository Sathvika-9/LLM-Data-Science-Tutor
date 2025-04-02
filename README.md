# Conversational AI Data Science Tutor with Streamlit and LangChain

This project is an AI-powered data science tutor built with Streamlit for an intuitive conversational interface and LangChain integrated with Google AI Studio for intelligent, context-aware responses. It allows users to ask data science-related questions and receive detailed, educational answers, leveraging the conversation history for continuity.

## Features

- User-friendly chat interface for asking questions
- AI-driven responses powered by Google's Gemini 2.0 flash model
- Context-aware answers that consider the full conversation history
- Detailed explanations, examples, and additional resources for learning
- Easy setup and local deployment

## Prerequisites

Before setting up the project, ensure you have the following:

- **Python 3.9 or higher** installed on your system
- A **Google AI Studio account** to obtain an API key

## Setup Instructions

Follow these steps to set up the project locally:

1. **Obtain an API Key**  
   - Sign up at [Google AI Studio](https://aistudio.google.com/apike/) and create a key.  
   - Generate an API key for the Gemini API.

2. **Set the Environment Variable**  
   - Store your API key securely as an environment variable named `GOOGLE_API_KEY`:  
     - On Unix-based systems (Linux/macOS):  
       ```bash
       export GOOGLE_API_KEY="your_api_key_here"
       ```  
     - On Windows:  
       ```bash
       set GOOGLE_API_KEY="your_api_key_here"
       ```

3. **Install Required Packages**  
   - Install the necessary Python packages using pip:  
     ```bash
     pip install langchain langchain-core langchain-google-genai streamlit 
     ```

## Running the App

Once the setup is complete, follow these steps to run the application:

1. Save the project code in a file, e.g., `app.py`.  
2. Open a terminal in the project directory and run the Streamlit app:  
   ```bash
   streamlit run app.py
   ```  
3. Your default web browser will automatically open to the app’s interface (typically at `http://localhost:8501`).

## Usage

Here’s how to use the Conversational AI Data Science Tutor:

1. **Ask a Question**: In the app’s chat input, type your data science-related question (e.g., "What is the difference between supervised and unsupervised learning?").  
2. **Get a Response**: The AI will analyze your question in the context of the conversation history and provide a detailed, educational response.

### Example

**User Query:**  
"What is the difference between supervised and unsupervised learning?"

**Expected Output:**  
```
### Supervised vs. Unsupervised Learning  
**Supervised Learning:** Involves training a model on labeled data, where the input-output pairs are known. The goal is to predict the output for new inputs. Examples include regression and classification.  
**Unsupervised Learning:** Involves training a model on unlabeled data to find hidden patterns or structures. Common tasks include clustering and dimensionality reduction.
```

## Customization

- Modify the system prompt in the `app.py` file to adjust the AI’s behavior or focus (e.g., emphasizing certain data science topics or adjusting the explanation complexity).

## Security

- The API key is stored as an environment variable (`GOOGLE_API_KEY`) rather than hardcoded in the script, ensuring better security.

## Troubleshooting

- **API Key Not Working**: Verify that `GOOGLE_API_KEY` is correctly set in your environment. Use `echo $GOOGLE_API_KEY` (Unix) or `echo %GOOGLE_API_KEY%` (Windows) to check.  
- **Package Errors**: Ensure all packages are installed and up-to-date with `pip install --upgrade streamlit langchain-google-genai`.  
- **Streamlit Won’t Start**: Confirm you’re running the correct command (`streamlit run app.py`) from the project directory.

## Contributing

Contributions are welcome! Feel free to submit pull requests with bug fixes, new features, or improvements.

---

**License**  
This project is licensed under the MIT License.
