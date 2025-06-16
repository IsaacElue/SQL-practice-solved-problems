
-- QUESTION 1
SELECT ABS(MAX(CASE
                   WHEN dept.department = 'marketing' THEN emp.salary
               END) - MAX(CASE
                              WHEN dept.department = 'engineering' THEN emp.salary
                          END)) AS salary_difference
FROM db_employee emp
JOIN db_dept dept ON emp.department_id = dept.id
WHERE dept.department IN ('marketing',
                          'engineering');


-- QUESTION 2
WITH max_salary AS (
    SELECT MAX(salary) AS highest_salary
    FROM worker
)

SELECT t.worker_title AS best_paid
FROM worker w
JOIN title t ON w.worker_id = t.worker_ref_id
JOIN max_salary m ON w.salary = m.highest_salary
ORDER BY best_paid;





