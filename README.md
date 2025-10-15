# MiniChain - Simple Blockchain Implementation

This project is a simple implementation of a blockchain in Python. It uses the Flask web framework to expose a REST API and a web interface for interacting with the blockchain.

## Features

-   **Genesis Block Creation**: The first block in the chain is created automatically.
-   **Transaction Pool**: Unconfirmed transactions are stored in a pool.
-   **Proof-of-Work Mining**: A simple Proof-of-Work algorithm is used to mine new blocks.
-   **Chain Validation**: A method is included to validate the integrity of the blockchain.
-   **Data Persistence**: The blockchain is automatically saved to `chain_data.json` and loaded on startup.
-   **REST API**: A simple API allows for adding transactions, mining new blocks, and viewing the chain.
-   **Web Interface**: A user-friendly web interface to interact with the blockchain.

## Setup and Usage

1.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

2.  **Run the Application**:
    ```bash
    python app.py
    ```
    The application will be running on `http://localhost:5000`.

## API Endpoints

-   **`GET /`**: Serves the web interface.
-   **`GET /mine`**: Mines a new block.
-   **`POST /transactions/new`**: Adds a new transaction to the pool.
    -   **Request Body**:
        ```json
        {
            "sender": "sender_address",
            "recipient": "recipient_address",
            "amount": 5
        }
        ```
-   **`GET /chain`**: Returns the full blockchain.

## Deployment on Render

This application is ready to be deployed on Render's free tier.

### Automatic Deployment with `render.yaml`

1.  **Fork this repository** to your own GitHub account.
2.  Go to the [Render Dashboard](https://dashboard.render.com/) and click **New +** > **Blueprint**.
3.  Connect your GitHub account and select your forked repository.
4.  Render will automatically detect the `render.yaml` file and configure the service.
5.  Click **Apply** to deploy the application.

### Manual Deployment

1.  **Fork this repository** to your own GitHub account.
2.  Go to the [Render Dashboard](https://dashboard.render.com/) and click **New +** > **Web Service**.
3.  Connect your GitHub account and select your forked repository.
4.  Configure the service:
    -   **Name**: `minichain` (or your preferred name)
    -   **Environment**: `Python 3`
    -   **Region**: Choose a region close to you.
    -   **Branch**: `main` (or your default branch)
    -   **Build Command**: `pip install -r requirements.txt`
    -   **Start Command**: `gunicorn app:app`
5.  Click **Create Web Service**.

**Note**: The free tier service will automatically sleep after a period of inactivity. It will wake up on the next request, which may cause a short delay.