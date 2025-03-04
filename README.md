# Financial_AI_Agent_Phidata
Building my First Financial AI Agent Using Phidata to Explore the Agentic AI

Steps to Setup and Run Application:
1) Use Cmd prompt:
    conda create -p venv python==3.12
    Give the required confirmation

2) We need to activate Conda environment
    conda activate venv/ 
        or
    conda activate C:\Users\Your_project_path\your_project_name\venv

3) Ensure pip is up to date using -> 
    python.exe -m pip install --upgrade pip

4) Now once you are into the venv, then check the requirements.txt file where execute it using below command
    pip install -r requirements.txt

    Note: If the above command works then proceed to next step, if it does't work then execute below command to manally install the contents of requirements.txt file in the venv

    pip install phidata python-dotenv yfinance packaging duckduckgo-search fastapi uvicorn groq

    check installed packages using -> pip list

5) Now Check you .env file is present or not and if not present the create .env file and add the API keys from  each site accordingly that is from phidata.com(https://www.agno.com/) and from Groq.com(https://groq.com/)
 a) for Phidata API key generation
    https://www.agno.com/ -> Login -> https://app.agno.com/ -> API Key -> Copy API key and use it on .env file at GROQ_API_KEY
 
 b) For Groq API key generation 
    https://groq.com/-> Login -> Developers -> Dev Console -> API Keys -> Create API Key -> Give a name to API key -> Copy and Store the API Key in your local as we need to use it in our .env at PHI_API_KEY

6) Now we need to run the content of the financial_agent.py file using -> python financial_agent.py , 
    Note:
    a) if you get an error to openapi, then install openai using 
        pip install openai

        if there is upgrade issue then -> pip install --upgrade openai

    b) if you still get an error after that, check the api keys by setting it as below using below command,
        setx GROQ_API_KEY YourGroqAPIKey

    c) if the issue related to openai still persists then, goahead an creare your openai api key from openai site and use it, by placing it in .env OPENAI_API_KEY=YOUR_OPENAI_KEY 
       and if you still face an issue with like above related to openai key then you can set it as above by using setx i.e,
        setx OPENAI_API_KEY YOUR_OPENAI_KEY
7) Finally run the python file as below, then we get the Summarized analysis of the latest news for NVDA
    python financial_agent.py
    
## Chatbot setup

8) With the help all the above setup we get the Required data in terminal, but when want our own chat bot then we try to run the playground.py file to work using below
    python playground.py

Note: If we get any error related to python-multipart, then run the below cmd and again run the above python application
    pip install python-multipart

9) After the above step if you hit local url that generated you will get error of not found, to fix that first you need to login to the phidata.com or agno.com and follow below steps
    Dashboard -> Playground -> Select an endpoint -> select "localhost:existingport"




