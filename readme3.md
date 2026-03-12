1. Contare quanti iscritti ci sono stati ogni anno
   ??
2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT
teachers.office_address,
COUNT(teachers.office_address) AS office_address
FROM `db-university`.teachers

GROUP BY teachers.office_address

3. Calcolare la media dei voti di ogni appello d'esame

SELECT \* FROM `db-university`.exam_student;
SELECT
exam_student.vote,
ROUND(AVG(exam_student.vote), 2) AS exam_vote
FROM `db-university`.exam_student

GROUP BY exam_student.vote

4. Contare quanti corsi di laurea ci sono per ogni dipartimento
