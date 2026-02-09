<h1 align="center">Hi 👋, I'm Julieta Pérez</h1>

SQL & Data Analysis Enthusiast from Argentina 🇦🇷


👩‍💻 About Me

🔭 Working on personal projects using SQL and Excel

🌱 Currently learning PostgreSQL & Database Administration

🎓 Studying for a Bachelor’s degree in Systems Analysis (UBA)

👯 Open to collaborate on SQL & database-related projects

💬 Ask me about SQL, Databases, Queries, Data Analysis


📂 Projects

👉 https://github.com/Julicss?tab=repositories
- 📄 Know about my experiences [www.linkedin.com/in/julieta-m-perez](www.linkedin.com/in/julieta-m-perez)
  

- 🧠 Sample SQL Code

- -- Project: Customer Orders Analysis

CREATE TABLE customers (
    customer_id SERIAL PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE orders (
    order_id SERIAL PRIMARY KEY,
    customer_id INT REFERENCES customers(customer_id),
    order_date DATE NOT NULL,
    total_amount NUMERIC(10,2) CHECK (total_amount >= 0)
);

-- Total revenue per customer
SELECT
    c.full_name,
    COUNT(o.order_id) AS total_orders,
    SUM(o.total_amount) AS total_spent
FROM customers c
JOIN orders o
ON c.customer_id = o.customer_id
GROUP BY c.full_name
ORDER BY total_spent DESC;


🛠️ Skills

SQL (queries, joins, subqueries)

PostgreSQL

MySQL

Excel (analysis & reports)

Git & GitHub


📫 Contact

📧 Email: julietaperez.it.art@gmail.com

💼 LinkedIn: www.linkedin.com/in/julieta-m-perez


