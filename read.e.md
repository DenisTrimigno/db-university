------ Query SELECT ---------

es.1
SELECT \* FROM 'students' WHERE YEAR('date_of_birth') = 1990;

es.2
SELECT \* FROM "courses WHERE "cfu' > 10;

es.3
SELECT \* FROM students WHERE YEAR(CURRENT DATE ()) - YEAR"date of birth') › 30;

es.4
SELECT \* FROM courses WHERE period = 'I semestre' AND year = 1;

es.5
SELECT \* FROM exams WHERE date = '2020-06-20' AND hour > '14:00:00';

es.6
SELECT \* FROM "degrees WhERE level = 'magistrale';

es.7
SELECT COUNT (\*) FROM departments;

es.8
SELECT COUNT (\*) FROM teachers WHERE phone IS NULL;

------- Query GROUP BY -----

es.1
SELECT YEAR(enrolment_date) as anno_iscrizione, COUNT(\*) as numero_studenti FROM students GROUP BY anno_iscrizione ORDER BY anno_iscrizione;

es.2
SELECT office_address as ufficio, COUNT(\*) as numero_insegnanti FROM teachers GROUP BY office_address ORDER BY office_address;

es.3
SELECT exam*id as appello_esame, AVG(vote) as media* voto FROM exam_student GROUP BY exam_id ORDER BY exam_id;

------ Query JOIN ---------

es.1
SELECT students. \* FROM students INNER JOIN degrees ON students.degree_id = degrees.id WHERE degrees.name = 'Corso di Laurea in Economia'

ES.2
SELECT degrees.\* FROM degrees INNER JOIN departments ON degrees.department id = departments.id WhErE departments.name = 'Dipartimento di Neuroscienze' AND degrees.level = 'magistrale';

es.3
SELECT courses.\*, teachers.name as nome*insegnante, teachers. surname as cognome_insegnante FROM courses INNER JOIN course_teacher ON courses. id = course_teacher.course_id INNER JOIN teachers ON course* teacher.teacher*id = teachers.id WHERE course* teacher. teacher_id = 44;

es.4
SELECT students.\*, degrees.name as corso_di_laurea, departments.name as dipartimento FROM students INNER JOIN degrees ON students.degree_id = degrees.id INNER JOIN departments ON degrees. department_id = departments. id ORDER BY Students.surname, students.name:
