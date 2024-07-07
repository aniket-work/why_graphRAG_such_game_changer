# Why graphRAG such a game changer 

## Introduction

This project demonstrates how AI enables one-person businesses, allowing anyone to become an entrepreneur or solopreneur. By leveraging AI tools, we can now handle complex tasks that previously required multiple experts. This README guides you through setting up and running an AI-powered Market Analysis business that uses AI for property classification and management.

## What's This Project About?

This project is a practical implementation of a one-person startup powered entirely by AI. It includes:

1. A Streamlit-based frontend for a Market Analysis management website
2. A Flask backend server that communicates with an AI model
3. AI-powered property classification for categorizing listings
4. A simple database system for storing property information

The project demonstrates how AI can automate tasks like property categorization, enabling efficient management of a Market Analysis business by a single person.

## Why Use This Project?

- Learn how to integrate AI into a real-world business application
- Understand the potential of AI in streamlining business operations
- Gain insights into building scalable, AI-powered web applications
- Explore how tasks typically requiring teams can be handled efficiently by AI

## Architecture

The project consists of the following components:

1. Frontend: Streamlit Web Application
2. Backend: Flask Web Server with RESTful API
3. Services: LLM Service for property classification, Database Service for data management
4. External Components: Groq API for LLM model access
5. Data Storage: JSON file (company_db.json)

**Prerequisites:**
- Python installed on your system.
- A basic understanding of virtual environments and command-line tools.

**Steps:**
1. **Virtual Environment Setup:**
   - Create a dedicated virtual environment for our project:
   
     ```bash
     python -m venv why_graphRAG_such_game_changer
     ```
   - Activate the environment:
   
     - Windows:
       ```bash
       why_graphRAG_such_game_changer\Scripts\activate
       ```
     - Unix/macOS:
       ```bash
       source why_graphRAG_such_game_changer/bin/activate
       ```
2. **Install Project Dependencies:**

   - Navigate to your project directory and install required packages using `pip`:
   
     ```bash
     cd path/to/your/project
     pip install -r requirements.txt
     ```

3. **Setup Keys : **

   - Obtain your Groq API key from [Groq Console](https://console.groq.com/keys).
   - Set your key in the `.env` file as follows:
   
     ```plaintext
    GROQ_API_KEY=<YOUR_KEY>       
    SERPER_API_KEY=KEY # https://serper.dev/     
    SEC_API_API_KEY=KEY # https://sec-api.io/ 
    
     ```

4. **Run the Market Analysis AI Application**

   Finally, execute the following command to start the Market Analysis AI application:

   ```bash   
   # Run UI
   streamlit run main.py
   ```  

