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

3. ## 3. Setup & Install

### a) Installing Ollama

1. Visit the official Ollama website: https://ollama.ai/
2. Download the appropriate version for your operating system (Windows, macOS, or Linux).
3. Follow the installation instructions provided for your OS.
4. Once installed, open a terminal or command prompt.
5. Verify the installation by running:
   ollama --version

To pull the Gemma 2B model using Ollama:
1. In the terminal, run:
   ollama pull gemma:2b
2. Wait for the download to complete. This may take some time depending on your internet speed.
3. Once downloaded, you can run the model using:
   ollama run gemma:2b

### b) Installing LM Studio

1. Go to the LM Studio website: https://lmstudio.ai/
2. Click on the "Download" button for your operating system.
3. Once the installer is downloaded, run it and follow the on-screen instructions.
4. After installation, launch LM Studio.
5. You may need to create an account or log in if prompted.

### c) Additional Setup

1. Ensure you have Python installed on your system (version 3.7 or higher is recommended).
2. You may need to install additional dependencies. Open a terminal and run:
   pip install torch transformers sentence-transformers
3. If you plan to use GPU acceleration, make sure you have the appropriate CUDA toolkit installed for your GPU.

### d) Verifying the Setup

1. Open a terminal and run: ollama list to see available models, including Gemma 2B.
2. Launch LM Studio and ensure you can access its interface.
3. In LM Studio, try loading a small model to verify it's working correctly.

### e) Configuring the Environment

1. Set up any necessary environment variables for your project.
2. Create a new directory for your GraphRAG project.
3. Initialize a new Python virtual environment in this directory:
   python -m venv graphrag_env
   source graphrag_env/bin/activate  # On Windows, use: graphrag_env\Scripts\activate
4. Install any additional Python libraries you'll need for your GraphRAG project.

### f) Testing the Setup

1. Write a simple Python script to test Ollama integration:
   import subprocess

   def query_ollama(prompt):
       result = subprocess.run(['ollama', 'run', 'gemma:2b', prompt], capture_output=True, text=True)
       return result.stdout

   response = query_ollama("What is GraphRAG?")
   print(response)
2. Run this script to ensure Ollama and the Gemma 2B model are working correctly.
       

4.  ** initialze graphRAG **

    ```bash
    python -m graphrag.index --init --root ragtest
    ```
5. ** Download data **
        1. Download from below link
        https://github.com/nihitx/game-of-thrones-/blob/master/gameofthrones.txt 
        2. save under "input" folder

5. ** Index **

    ```bash
    python -m graphrag.index --root .\ragtest
    ```
5. **Run Query**

   ```bash   
   python -m graphrag.query --root .\ragtest --method global "How was impact of Lily action on villagers"
   
   ```  

