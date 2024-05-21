# 🧊 Freeze Frame - Snowflake Arctic AI Chatbot ❄️
Unlock valuable data insights from both text and images with Freeze Frame, an AI-powered chatbot featuring advanced graph analysis; built with Snowflake's brand new foundation model: Snowflake Arctic! Arctic was released on April 24, 2024 and is completely open-source. :)

This essential AI tool seamlessly analyzes textual queries and graphical data, transforming data interaction and decision-making for businesses and simplifying the extraction of valuable information for researchers.

Get the full lowdown on Arctic in Adrien Treuille's [blog post](http://blog.streamlit.io/introducing-snowflake-arctic/). Snowflake Arctic is also available via [Hugging Face](https://huggingface.co/Snowflake/snowflake-arctic-instruct) 🤗 and all your favorite model gardens soon!

![Freeze Frame Streamlit app chatbot for Snowflake Arctic](Streamlit-Arctic-Screenshot.png)

## Getting your own Replicate API token

To use this app, you'll need to get your own [Replicate](https://replicate.com/) API token.

After creating a Replicate account, you can access your API token from [this page](https://replicate.com/account/api-tokens).

## Setup Instructions

### Prerequisites
- Python 3.8 or later 🐍
- pip3 📦

### Installation
1. **Clone this repository**
   ```bash
   git clone https://github.com/yourusername/snowflake-arctic-st-freezeframe.git
   cd snowflake-arctic-st-freezeframe
   ```

2. **Install requirements**
   ```bash
   pip install -r requirements.txt
   ```
   Note: you may need one or more external dependencies. Some of these can be found in the `packages.txt` file.

3. **Add your API token to your secrets file**\
Create a `.streamlit` folder with a `secrets.toml` file inside.
   ```bash
   mkdir .streamlit
   cd .streamlit
   touch secrets.toml
   ```
   
   Use your text editor or IDE of choice to add the following to `secrets.toml`:
      ```toml
      REPLICATE_API_TOKEN = "your API token here"
      ```
   Learn more about Streamlit secrets management in the [Streamlit docs](https://docs.streamlit.io/deploy/streamlit-community-cloud/deploy-your-app/secrets-management).
   
   Alternatively, you can enter your Replicate API token via the `st.text_input` widget in the app itself (once you're running the app).

4. **Run the Streamlit app**\
To run the app, enter:
   ```bash
   cd ..
   streamlit run streamlit_app.py
   ```

### Deployment
Host your app for free on Streamlit Community Cloud. These instructions are also available in the [Streamlit docs](https://docs.streamlit.io/deploy/streamlit-community-cloud/deploy-your-app).

1. Sign up for a Community Cloud account or log in at [share.streamlit.io](https://share.streamlit.io/).
2. Click "New app" from the upper-right corner of your workspace.
3. Fill in your repo, branch, and file path. As a shortcut, you can also click "Paste GitHub URL" to paste a link directly to `streamlit_app.py` on GitHub.  

#### Optional: store your Replicate API token with Community Cloud secrets
Securely store your Replicate API token with Community Cloud's secrets management feature. These instructions are also available in the [Streamlit docs](https://docs.streamlit.io/deploy/streamlit-community-cloud/deploy-your-app/secrets-management).
   
##### Add secrets before deploying
1. Before clicking "Deploy", click "Advanced settings..."  
2. A modal will appear with an input box for your secrets.   
3. Provide your secrets in the "Secrets" field using TOML format. For example:
   ```toml
   REPLICATE_API_TOKEN = "your API token here"
   ```
   
##### Add secrets after deploying
1. Go to [share.streamlit.io](https://share.streamlit.io/).
2. Click the overflow menu icon (AKA hamburger icon) for your app.
3. Click "Settings".  
4. A modal will appear. Click "Secrets" on the left.  
5. After you edit your secrets, click "Save". It might take a minute for the update to be propagated to your app, but the new values will be reflected when the app re-runs.
