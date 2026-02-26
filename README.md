# RTS_ERL_Dataset

##  Overview

**RTS_ERL_Dataset** is a structured dataset designed to power a **Bangla E-commerce RAG (Retrieval-Augmented Generation) Chatbot**.

The dataset mimics real-world e-commerce product data in natural language format, making it suitable for:

-  AI-powered product search
-  Bangla conversational agents
-  Semantic search systems
-  Recommendation systems
-  LLM fine-tuning & RAG pipelines

This dataset is optimized for use with **MongoDB + Vector Search systems** (e.g., FAISS) in modern AI stacks.

---

##  Dataset Structure

The dataset simulates real e-commerce product entries including:

| Field | Description |
|---|---|
| `Product_id` | unnique ID of the product |
| `Product Name` | Name of the product |
| `Category` | Product category |
| `Price` | Product price |
| `Description` | Natural Bangla language description in English |
| `Features` | Key product features as an array |
| `Brand` | Brand name |
| `stock_status` | Stock availability status |

Each document is structured for:
- Direct MongoDB storage
- Embedding generation
- Semantic similarity search

---

##  How to Access the Data?

### Option 1: Using MongoDB Compass (Recommended) 

MongoDB Compass is the easiest way to access this dataset. It provides a clean visual interface to browse, filter, and export data without writing any code.

#### Step 1: Install MongoDB Compass

Download and install [MongoDB Compass](https://www.mongodb.com/try/download/compass) — the official desktop GUI for MongoDB.


#### Step 2: Get Your Credentials

>  **Note:** Due to security reasons, the full MongoDB URI cannot be shared in this repository. The credentials (username & password) will be provided separately.

Secure connection string format:
```
mongodb+srv://<username>:<password>@cluster0.mongodb.net/
```

---

#### Step 3: Connect via MongoDB Compass

1. Open **MongoDB Compass**
2. Click **"Add New Connection"**
3. Paste your connection string into the URI field
4. Click **"Save & Connect"**

---

#### Step 4: Access the Dataset

Once connected, navigate to:

```
Database  →  new_product
Collection →  new_products
```

You will now see all the product documents ready to browse, query, or export.

---


### Option 2: Using MongoDB Atlas (Cloud)

If you prefer a browser-based experience, you can access the data directly through MongoDB Atlas.

#### Step 1: Create an Atlas Account

1. Go to [MongoDB Atlas](https://www.mongodb.com/atlas) and create a free account
2. Create a new **cluster**
3. Create a **database user** with a username and password
4. Whitelist your **IP address** under Network Access
5. Copy your **connection string** from the Atlas dashboard

#### Step 2: Browse the Dataset

Once your cluster is set up, navigate to:
```
Database  →  new_product
Collection →  new_products
```

---


### Option 3: Using a Local MongoDB Instance

#### Step 1: Install MongoDB Locally

Download and install:
- [MongoDB Community Edition](https://www.mongodb.com/try/download/community)
- [MongoDB Compass](https://www.mongodb.com/try/download/compass)

#### Step 2: Start the MongoDB Service

| OS | Command |
|---|---|
| Windows | Starts automatically as a background service |
| macOS / Linux | Run `mongod` in your terminal |

#### Step 3: Connect via Compass

Open Compass and connect using the default local URI:
```
mongodb://localhost:27017
```

#### Step 4: Import the Dataset

Use MongoDB Compass's **"Import Data"** feature or run:
```bash
mongorestore --db new_product <path-to-dataset>
```

---

##  Intended Use

| Use Case | Description |
|---|---|
| RAG Chatbot | Primary use — retrieval-augmented Bangla chatbot |
| NLP Research | Bangla e-commerce language modeling |
| LLM Fine-tuning | Domain-specific fine-tuning on product data |
| Semantic Search | Vector-based similarity search over products |

---

##  Contact

For questions, issues, or collaboration requests, please open an [issue](../../issues) in this repository.
