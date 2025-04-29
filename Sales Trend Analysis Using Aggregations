use sales;
-- Sample orders table
CREATE TABLE online_sales (
    order_id INT,
    order_date DATE,
    amount DECIMAL(10,2),
    product_id INT
);

-- Insert example data
INSERT INTO online_sales VALUES
(1, '2024-01-15', 100.00, 101),
(2, '2024-01-20', 150.00, 102),
(3, '2024-02-05', 200.00, 103),
(4, '2024-02-15', 130.00, 104),
(5, '2024-03-01', 180.00, 101),
(6, '2024-03-10', 220.00, 102),
(7, '2024-03-15', 120.00, 105);
-- Monthly Revenue & Sales Volume Query
SELECT
  EXTRACT(YEAR FROM order_date) AS year,
  EXTRACT(MONTH FROM order_date) AS month,
  SUM(amount) AS total_revenue,
  COUNT(DISTINCT order_id) AS order_volume
FROM online_sales
GROUP BY
  EXTRACT(YEAR FROM order_date),
  EXTRACT(MONTH FROM order_date)
ORDER BY year, month;
SELECT
  EXTRACT(YEAR FROM order_date) AS year,
  EXTRACT(MONTH FROM order_date) AS month,
  SUM(amount) AS total_revenue,
  COUNT(DISTINCT order_id) AS order_volume
FROM online_sales
WHERE order_date BETWEEN '2024-01-01' AND '2024-03-31'
GROUP BY
  EXTRACT(YEAR FROM order_date),
  EXTRACT(MONTH FROM order_date)
ORDER BY total_revenue DESC;
