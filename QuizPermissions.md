### Quiz App Permissions

**IsCourseMember**

> return True if request.user is member of the course for given quiz or quiz box, else return False

> Applied for QuizBox, Quiz, QuizDetail, Question, QuestionDetail, MyQuizGradeBox, GradeQuestion, GradeQuiz

**IsCourseMemberForList**

> return True if requets.user is member of course, else return False

> Applied for Quiz, Question, MyQuizGradeBox

**IsCourseOwnerOrReadOnly**

> return True, if request.method is in GET, HEAD, OPTIONS

> return True, if request.method is not in GET, HEAD, OPTIONS, and request.user is teacher of the course, else return False

> Applied for Quiz, QuizDetail

**IsCourseOwnerOrNotAllowed**

> return True if request.user is teacher of the course, else return False

> Applied for AllStudentsGrade

**IsNotSubmitted**

> return True if grade object is not yet submitted, else return False

> Applied for GradeQuiz

**DueIsOver**

> return True if grade object due is not yet passed, else return False

> Applied for GradeQuiz