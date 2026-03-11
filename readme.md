1. Selezionare tutti gli studenti nati nel 1990 (160)

SELECT COUNT(\*) FROM `db-university`.students
WHERE students.date_of_birth LIKE "1990%";

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

SELECT COUNT(\*) FROM `db-university`.courses
WHERE courses.cfu > 10;

3. Selezionare tutti gli studenti che hanno più di 30 anni

SELECT \* FROM `db-university`.students
WHERE
YEAR(students.date_of_birth) < 1995;

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
   laurea (286)

SELECT COUNT(\*) FROM `db-university`.courses
WHERE courses.year LIKE 1 AND courses.period LIKE "I semestre";

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
   20/06/2020 (21)

SELECT COUNT(\*) FROM `db-university`.exams
WHERE
exams.date LIKE "2020-06-20" AND exams.hour > "13%";
;

6. Selezionare tutti i corsi di laurea magistrale (38)

SELECT COUNT(\*) FROM `db-university`.degrees
WHERE degrees.level LIKE "magistrale";

7. Da quanti dipartimenti è composta l'università? (12)

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
