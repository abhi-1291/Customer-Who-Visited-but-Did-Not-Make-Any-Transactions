SELECT customer_id, COUNT(Visits.visit_id) AS count_no_trans
<br>
FROM Visits
<br>
LEFT JOIN Transactions
<br>
ON Visits.visit_id = Transactions.visit_id
<br>
WHERE transaction_id IS null
<br>
GROUP BY customer_id;
