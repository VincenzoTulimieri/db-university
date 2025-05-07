# Query group by

## 1. Contare quanti iscritti ci sono stati ogni anno
```
SELECT YEAR(`enrolment_date`) AS `enorlment_year`, COUNT(*) AS `number_students`

FROM `students`

GROUP BY YEAR(`enrolment_date`);
```
## 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
```
SELECT COUNT(*) AS `numbers_teachers`, `office_address`

FROM `teachers`

group by `office_address`;
```
## 3. Calcolare la media dei voti di ogni appello d'esame
```
SELECT AVG(`vote`) AS `average_grades`

FROM `exam_student`

GROUP BY `exam_id`;
```
## 4. Contare quanti corsi di laurea ci sono per ogni dipartimento
```
SELECT COUNT(*) AS `numbers_courses`, `department_id`

FROM `degrees`

GROUP BY `department_id`;
```