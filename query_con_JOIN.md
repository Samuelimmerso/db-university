<!--

-- 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia


  SELECT *
  FROM `students`
  INNER JOIN `degrees`
  ON `students`.`degree_id` = `degrees`.`id`
  WHERE `degrees`.`id`='53';



-- 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)



  SELECT * FROM `course_teacher`
  INNER JOIN `courses`
  ON `course_teacher`.`course_id` = `courses`.`id`
  WHERE `course_teacher`.`teacher_id`='44';





-- 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome



  SELECT * FROM `students`
  INNER JOIN `degrees`
  ON `students`.`degree_id` = `degrees`.`id`
  INNER JOIN `departments`
  ON `degrees`.`department_id` = `departments`.`id`
  ORDER BY `students`.`surname` ASC;














