# SQL-Questions-and-solutions
Q.1 leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions
select v.customer_id as customer_id, count(*) as count_no_trans
from visits v 
left join transactions t
on v.visit_id = t.visit_id
where t.transaction_id is null
group by customer_id
