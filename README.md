# AI-Powered SQL and Tabular Data Chatbot

## Project Overview

The **SQL and Tabular Data Chatbot** is an AI-powered application that enables users to interact with structured datasets using natural-language questions instead of writing SQL queries manually.

Users can upload CSV or Excel files, and the system processes the uploaded data and converts it into SQL tables. By integrating LangChain with the Groq API, the chatbot interprets user questions, generates appropriate SQL queries, retrieves relevant information from the database, and presents the results in an understandable format.

The application provides a simple and interactive interface using Gradio, making data analysis more accessible to users without SQL knowledge.

## Key Features

- **File Upload:** Supports uploading CSV and Excel datasets.
- **Automated Data Processing:** Reads and processes tabular data using Pandas.
- **SQL Database Integration:** Converts uploaded datasets into SQL tables.
- **Natural-Language Querying:** Allows users to ask questions in ordinary English.
- **AI-Powered SQL Generation:** Uses LangChain and Groq API to generate SQL queries.
- **Automated Data Retrieval:** Executes generated SQL queries against the uploaded database.
- **Interactive Chat Interface:** Displays answers through a Gradio-based interface.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend development |
| Gradio | User interface |
| Pandas | Data processing |
| LangChain | LLM and SQL workflow integration |
| Groq API | Language model access |
| ChatGroq | LangChain integration with Groq |
| SQLite | Database management |
| SQLAlchemy | Database connectivity |

## System Workflow

1. The user uploads a CSV or Excel dataset.
2. Pandas reads and processes the uploaded file.
3. The dataset is converted into SQL tables.
4. The user enters a question in natural language.
5. LangChain coordinates the interaction with the Groq language model.
6. The language model generates an appropriate SQL query.
7. The SQL query is executed against the database.
8. The retrieved results are converted into a readable response.
9. The final answer is displayed through the Gradio interface.

## System Architecture

The application follows a modular architecture consisting of:

- **Presentation Layer:** Gradio interface for file uploads and chatbot interaction.
- **File Processing Layer:** Handles CSV and Excel data using Pandas.
- **Application Layer:** Manages chatbot logic and user requests.
- **AI Processing Layer:** Uses LangChain and Groq API for natural-language understanding and SQL generation.
- **Database Layer:** Stores uploaded datasets and executes SQL queries.
- **Response Layer:** Returns database results as understandable answers.

## Project Structure

```text
SQL-and-Tabular-Data-Chatbot/
│
├── app.py
├── configs/
│   └── app_config.yml
│
├── utils/
│   ├── chatbot.py
│   ├── upload_file.py
│   ├── load_config.py
│   ├── prepare_sqlitedb_from_csv_xlsx.py
│   └── prepare_vectordb_from_csv_xlsx.py
│
├── requirements.txt
├── .env
└── README.md
```

*Note: The structure above is illustrative. Adjust filenames and folders to match your actual repository.*

## Installation and Setup

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the Project Directory

```bash
cd SQL-and-Tabular-Data-Chatbot
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure the Groq API Key

Create a `.env` file in the project root directory and add your API key using the environment variable name expected by your application.

```env
GROQ_API_KEY=your_groq_api_key
```

Obtain an API key from the [Groq Console](https://console.groq.com/).

**Important:** Never upload your actual API key or `.env` file to GitHub.

### 6. Run the Application

```bash
python app.py
```

Open the local URL displayed in the terminal, usually:

```text
http://127.0.0.1:7860
```

## Example Use Case

Consider uploading a movie dataset containing:

- Movie names
- Genres
- Release years
- Ratings

Users can ask questions such as:

- Which movie has the highest rating?
- Display the top five movies.
- How many movies were released after 2020?
- What is the average rating of all movies?

The chatbot processes these questions, retrieves information from the uploaded dataset, and displays the results.

## Advantages

- Reduces the need to write SQL queries manually.
- Makes structured-data analysis easier for non-technical users.
- Supports interactive querying of uploaded datasets.
- Combines language models with traditional SQL database operations.
- Provides a simple and accessible interface.

## Future Enhancements

- Support for additional database systems.
- Improved handling of complex SQL queries.
- Enhanced data visualisation and reporting.
- Better query validation and error handling.
- Improved security and access control.
- Support for larger datasets and performance optimisation.

## Author

**Project:** AI-Powered SQL and Tabular Data Chatbot

**Domain:** Artificial Intelligence | Natural Language Processing | Database Management

**Technologies:** Python, Gradio, LangChain, Groq API, Pandas and SQL

## License

This project is intended for educational and learning purposes.# Chatbot
