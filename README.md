# Odoo Product Description Updater

This Python script fetches product details from an Odoo database and automatically generates product descriptions using OpenAI's GPT-3 engine.

## Features

- Fetch products from an Odoo database
- Generate product descriptions using OpenAI's GPT-3
- Update the product descriptions back into the Odoo database

## Requirements

- Python 3.x
- `openai` Python package
- `xmlrpc.client` (standard library)
- `ssl` (standard library)
- `configparser` (standard library)

## Setup

1. **Install Dependencies**: If you haven't installed the OpenAI Python package, install it using pip:
    ```bash
    pip install openai
    ```

2. **Configuration**: Create a `config.ini` file in the same directory as your Python script and add your OpenAI API key and Odoo database credentials. Here's an example:

    ```ini
    [OpenAI]
    api_key = YOUR_OPENAI_API_KEY

    [Odoo]
    url = YOUR_ODOO_URL
    db = YOUR_DATABASE_NAME
    username = YOUR_USERNAME
    password = YOUR_PASSWORD
    ```

    Make sure to replace `YOUR_OPENAI_API_KEY`, `YOUR_ODOO_URL`, `YOUR_DATABASE_NAME`, `YOUR_USERNAME`, and `YOUR_PASSWORD` with your actual credentials.

3. **Prevent Accidental Upload**: To prevent accidentally uploading your `config.ini` file, add it to a `.gitignore` file:
    ```ini
    config.ini
    ```

## Usage

Run the script with Python:

```bash
python your_script_name.py
```

The script will log into the Odoo database, fetch the first 100 products, generate descriptions for them using OpenAI's GPT-3, and then update these descriptions back into the database.
