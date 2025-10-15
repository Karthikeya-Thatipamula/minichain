# ⛓️ MiniChain - A Simple Blockchain Implementation

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status: Active](https://img.shields.io/badge/status-active-success.svg)

A lightweight, educational blockchain built with Python and Flask. This project provides a simple, hands-on introduction to the core concepts of blockchain technology, including mining, transactions, and proof-of-work.

**[Live Demo](https://minichain-szyk.onrender.com/)**

---

### ✨ Features

-   **Proof-of-Work (PoW):** Simple PoW algorithm to secure the network.
-   **Transaction Pool:** Manages unconfirmed transactions before they are mined into a block.
-   **Chain Validation:** Ensures the integrity and immutability of the blockchain.
-   **Data Persistence:** Saves the blockchain state to a JSON file (`chain_data.json`) and loads it on startup.
-   **RESTful API:** A clean API for interacting with the blockchain programmatically.
-   **Modern Web UI:** A sleek, dark-themed dashboard to visualize the chain, add transactions, and mine new blocks.

### 💻 Tech Stack

-   **Backend:** Python, Flask
-   **Frontend:** HTML, CSS, JavaScript (jQuery)
-   **Deployment:** Gunicorn, Render

### 🚀 Getting Started

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/MiniChain.git
    cd MiniChain
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the application:**
    ```bash
    python app.py
    ```
    The application will be available at `http://localhost:5000`.

### 🔗 API Endpoints

-   `GET /`: Serves the web interface.
-   `GET /chain`: Returns the entire blockchain.
-   `GET /mine`: Mines a new block.
-   `POST /transactions/new`: Adds a new transaction to the pool.
-   `GET /transactions/pending`: Returns the list of unconfirmed transactions.

### ☁️ Deployment

This project is configured for easy deployment on [Render](https://render.com/) via the provided `render.yaml` file.

1.  **Fork the repository.**
2.  On the Render Dashboard, click **New +** > **Blueprint**.
3.  Connect your GitHub and select the forked repository. Render will automatically configure the deployment.

### 🤝 Contributors

-   **Karthikeya Thatipamula** (Lead)
-   [Shivam Patel](https://github.com/Shivam-Patel-G)
-   Aryan Sohani
-   [Shashank Gupta](https://github.com/shashankpc7746)

---

<p align="center">
  <em>Made for educational purposes.</em>
</p>