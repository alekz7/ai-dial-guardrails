# Project Overview

This project provides a series of tasks for building and testing AI guardrails in Python. The primary focus is on preventing prompt injection attacks and leakage of Personally Identifiable Information (PII). The tasks progressively introduce different guardrail techniques, including input validation, output validation, and real-time streaming protection.

The project is structured as a series of Python scripts, each representing a different task or sub-task. The user is expected to complete the `TODO` sections in each file to implement the guardrails.

**Key Technologies:**
- Python 3.11+
- LangChain
- Presidio
- AzureChatOpenAI

## Building and Running

1.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

2.  **Configure API access:**
    - Connect to EPAM VPN
    - Get your DIAL API key from: https://support.epam.com/ess?id=sc_cat_item&table=sc_cat_item&sys_id=910603f1c3789e907509583bb001310c
    - Set the `DIAL_API_KEY` environment variable:
      ```bash
      export DIAL_API_KEY='your-api-key'
      ```

3.  **Run a specific task:**
    Each task is a self-contained Python script that can be run directly. For example, to run the first task:
    ```bash
    python tasks/t_1/prompt_injection.py
    ```

## Development Conventions

-   **API Keys:** API keys are managed through environment variables. The `tasks/_constants.py` file defines the DIAL_URL and retrieves the API_KEY from the `DIAL_API_KEY` environment variable.
-   **Testing:** The project encourages a test-driven approach. The `tasks/PROMPT_INJECTIONS_TO_TEST.md` file provides a comprehensive list of prompt injection techniques to test the implemented guardrails.
-   **Modularity:** The tasks are organized into separate directories, each with its own `__init__.py` file, promoting modularity and separation of concerns.
-   **Progressive Difficulty:** The tasks are designed to be completed in a specific order, starting with basic prompt injection defense and progressing to more advanced techniques like streaming PII filtering.
-   **Frameworks:** The project leverages LangChain for LLM interactions and Presidio for PII detection and anonymization.
