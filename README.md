# Analyzing-Students-Mental-Health
--Overall, this SQL query provides insights into the academic performance of international students, including the number of students and their average scores in ------different areas, categorized by the length of their stay.
-- Start coding here...
-- Find the number of international students and their average scores by length of stay, in descending order of length of stay
SELECT stay, 
       COUNT(*) AS count_int,
       ROUND(AVG(todep), 2) AS average_phq, 
       ROUND(AVG(tosc), 2) AS average_scs, 
       ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;
