<h1 align="center"> Text Sentiment Analysis using Caikit and Hugging Face

<p align="center"> Cognitive Class AI ✨
  
### What is Caikit?

  Caikit is an AI toolkit that enables users to manage models through a set of developer friendly APIs. It provides a consistent format for creating and using AI models against a wide     variety of data domains and tasks.
  
### Mentee assignment ⏱️

   * Task for Mentee from IBM Advance AI Mentor @ Infinite Learning Course 🌐

   * Completed Course: Practice to Create Text Sentiment Analysis using Caikit and Hugging Face from CognitiveClass.ai 💻

### Tech Stack & Tools 👩‍💻
  <p align="center">
    <a
    <p>
<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
   </p>

  <p align="center">
  <a

[![Visual Studio](https://badgen.net/badge/icon/visualstudio?icon=visualstudio&label)](https://visualstudio.microsoft.com)
<img src="https://img.shields.io/badge/-Hugging%20Face-F7B8D3?style=flat&logo=hugging-face&logoColor=black" />
   </p>

### Documentation 📂
1. Install the requirements

       pip install -r requirements.txt

2. Start the runtime

       python start_runtime.py

3. Run the sentiment analysis in another terminal tab

       python client.py

### Procedure 💡

1. Create Project:
   Prepare the necessary directories and files for your project.
  
        pip install --user virtualenv
        mkdir -p /home/project/text-sentiment
        cd /home/project/text-sentiment

2. Define Model Data Specifications:
   Define the data format used by the Caikit module.
   
        mkdir data_model
        cd data_model
        touch classification.py

3. Create Model Wrapper:
   Implement a wrapper that integrates the AI model with the Caikit framework.

        mkdir -p models/text_sentiment
        cd models/text_sentiment
        touch config.yml
        mkdir runtime_model
        cd runtime_model
        touch hf_module.py
        touch __init__.py
        cd ../../..
    
4. Include Modules and Dependencies:
   Determine the dependencies needed for your project configuration.

        touch requirements.txt
        virtualenv -p python3 env
        source env/bin/activate
        pip install -r requirements.txt

        # requirements.txt
        caikit
        transformers

5. Start Caikit Runtime:
   Launch the Caikit runtime to serve the model for inference.

       touch start_runtime.py
       python start_runtime.py

       # start_runtime.py
        from caikit.runtime import start_runtime

        if __name__ == "__main__":
            start_runtime()

7. Sentiment Analysis Testing:
   Run tests to validate the sentiment analysis model's functionality through a client application.

       touch client.py
       python client.py

       # client.py
        import requests
   
        url = "http://localhost:5000/predict"  # Sesuaikan URL dengan alamat runtime Anda # Example
        data = {"text": "I love this product!"}
        
        response = requests.post(url, json=data)
        print("Response:", response.json())

