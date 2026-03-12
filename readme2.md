1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT
students.name students_name,
students.surname students_surname,
students.date_of_birth students_date_of_birth,
students.registration_number students_registration_number,
students.email students_email,
degrees.name degree_name

FROM `db-university`.students
INNER JOIN `db-university`.degrees
ON degree_id = degrees.id
WHERE degrees.name LIKE "%Economia%"

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
   Neuroscienze

   SELECT
   degrees.name degrees_name,
   departments.name departments_name

FROM `db-university`.degrees
LEFT JOIN `db-university`.departments
ON departments.id = department_id
WHERE departments.name LIKE "%Neuroscienze%"

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

SELECT \* FROM `db-university`.course_teacher
WHERE teacher_id = 44

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
   sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
   nome

SELECT
students.degree_id students_degree_id,
students.name students_name,
students.surname students_surname,
degrees.id degrees_id,
degrees.name degrees_name,
departments.id departments_id,
departments.name departments_name
FROM `db-university`.students

INNER JOIN `db-university`.degrees, `db-university`.departments

WHERE students.degree_id LIKE degrees.id
ORDER BY students.name

5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
   SELECT
   degrees.id degrees_id,
   degrees.name degrees_name,
   courses.id courses_id,
   courses.name courses_name,
   courses.description courses_description
   FROM `db-university`.degrees

INNER JOIN `db-university`.courses
ON courses.id = degrees.id
?? 6. Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica (54)
??

7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
   per ogni esame, stampando anche il voto massimo. Successivamente,
   filtrare i tentativi con voto minimo 18.
