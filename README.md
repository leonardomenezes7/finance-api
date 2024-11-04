# 💰 Finance API

I developed an API using Node.js, TypeScript, and PostgreSQL that allows users to register personal financial transactions. The recorded data includes the transaction name, amount, and type, which can be either credit or debit. This structure facilitates personal finance management by enabling each user to track and organize their financial movements efficiently.

## 📂 Project
![project](https://github.com/user-attachments/assets/ebc83f61-dbb9-4ec6-ba3e-f64bf901f15e)

### 🟢 Status: Development completed

## ⚙️ Features
- Create a transaction: Allows users to create a new transaction.
- List Transactions: Allows users to list all the transactions they created.
- List Transaction: Allows the user to list a single transaction they made.
- Get summary: Allows the user to view a summary of all transactions they made.

## 🛠️ Technologies Used
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![PostgresSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Node.js](https://img.shields.io/badge/Node%20js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![fastify](https://img.shields.io/badge/fastify-202020?style=for-the-badge&logo=fastify&logoColor=white)

## 💾 Database Structure
<img width="100%" alt="Captura de Tela 2024-11-04 às 02 17 51" src="https://github.com/user-attachments/assets/cd5076cd-1ceb-4b50-9d0c-1ac86d5a2a5b">

## 🎛️ Bussiness Rules
- `id` Unique identifier for each transaction
- `session_id` Identifier of the user who created the transaction
- `title` Transaction title
- `amount` Transaction amount
- `created_at` Timestamp when the transaction was created

## ↔️ Routes
- `POST /transactions` Creates a transaction in the database by sending `title`, `amount`, and `type` through the request body. If the `type` is equal to credit, a positive value will be added to the database; if `type` is debit, a negative value will be added. The fields `session_id` and `created_at` are automatically sent.
- `GET /transactions` Lists all transactions by the user’s `session_id` as request cookies.
- `GET /transactions/:id` Lists a specific transaction by the user’s `session_id` from request cookies and the transaction `id` from request params.
- `GET /transactions/summary` Shows the summary of the user’s transactions by `session_id` from request cookies.

## 🚀 How To Run
```bash
# Clone the project to the desired location on your computer.

```
