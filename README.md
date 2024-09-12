# ✉️ Cold Email Customization Using Llama 3 and ChromaDB

This project is a cold email generator designed for software service companies, utilizing `Llama 3-70B`, Groq, LangChain, and Streamlit. The tool enables users to input the URL of a company's careers page, automatically extracting job listings and generating tailored cold emails. These emails feature relevant portfolio links sourced from a vector database based on the specific job descriptions.

## Scenario Example

Imagine this scenario:

IBM is searching for a Principal Software Engineer and invests significant time and resources into the hiring process, onboarding, and training new employees. Meanwhile, a software development company can provide dedicated software engineers directly to IBM. To approach IBM, a business development executive from the software company will use this tool to generate a customized cold email, making the outreach more relevant and impactful.

## Features

- **Automated Web Scraping:** Extracts job roles, skills, and descriptions from career pages using the LangChain framework.
- **Personalized Email Generation:** Uses Llama 3 to create tailored emails with specific job roles and relevant portfolio links fetched from ChromaDB.
- **Faster Response Times:** Integrated with Groq to leverage their LPUs for quicker inference, enhancing the overall performance of the email generation process.
- **User-Friendly Interface:** Built with Streamlit to provide a straightforward UI for entering URLs and generating customized cold emails.

## Setup

1. **Get Started:** Obtain an API key from [Groq Console](https://console.groq.com/keys). Update the value of `GROQ_API_KEY` in the `app/.env` file with your generated API key.

2. **Install Dependencies:** Clone the repository and install the required dependencies by running:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Application:** Launch the Streamlit app with the following command:
    ```bash
    streamlit run app/main.py
    ```

## Project Structure

- **`app/`**: Contains the main application code, including the Streamlit UI and scripts for data processing.
- **`resources/`**: Includes supporting files such as CSVs for ChromaDB and additional configuration files.
- **`chains.py`**: Handles interactions with Llama 3 for email generation.
- **`portfolio.py`**: Manages the portfolio data using ChromaDB, linking relevant skills to portfolio URLs.

