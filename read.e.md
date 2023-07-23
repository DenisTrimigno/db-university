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
