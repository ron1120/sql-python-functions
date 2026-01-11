# SQL Python Functions

This repository contains Python scripts that interact with a PostgreSQL database to manage users, products, and orders.  
It includes functions to update orders and perform common database operations using SQL from Python.

## 📦 Features

- Connects to a PostgreSQL database running in Docker
- Python functions for:
  - Updating orders
  - Managing users and products
- Uses `psycopg2` to communicate with PostgreSQL

## 🚀 Getting Started

### Prerequisites

Install the following:

- Python 3.x  
- Docker (for running PostgreSQL)  
- `psycopg2-binary` for database interaction

---

## 📌 Setup Guide

### 1. Clone the repo

```bash
git clone https://github.com/ron1120/sql-python-functions.git
cd sql-python-functions

---

### 2. Create & activate a Python virtual environment

python3 -m venv venv
source venv/bin/activate       # Mac / Linux

### 3. Install dependencies

pip install -r requirements.txt


---

### Use Docker to run PostgreSQL🐘

docker run -d \
  --name my_postgres_db \
  -e POSTGRES_USER=myuser \
  -e POSTGRES_PASSWORD=mypassword \
  -e POSTGRES_DB=storedb \
  -p 5432:5432 \
  postgres:13


# Info:
	use docker cp to copy database into the container example:
		docker cp init_db.sql dd0c591dd22c:/init_db.sql


---




### Use Python Script🐍

python update_orders.py \
  --user david@example.com \
  --product "Kosher Wine" \
  --quantity 2












