### Permissions & Validation

**IsSuperUser**

> if request.user is superuser, return True
> else return False

> Yet Applied to views.

**IsTeacher**

> if request.user is teacher, return True
> else return False

> parent class for IsTeacherOrReadOnly class

**IsTeacherOrReadOnly**

> if request.method is POST and request.user is teacher, return True
> if request.method is POST and request.user is not teacher, return False
> else return True

> Applied to CourseList

> Subclassing IsTeacher class

**IsOwnerOrReadOnly**

> if request.method is POST and request.user is owner - here, author of ArticelModel or teacher of Course - return True
> if request.method is POST and request.user is not owner of model, return False
> else return True

> Applied to CourseDetail, ArticleDetail, CommentDetail(plan)

**IsMemberOfCourseOrNotAllowed**

> if request.user is member of course - here, member means either teacher or students of the Course - , return True
> else return False

> Applied to ArticleList, ArticleDetail, CommnetList(plan), CommentDetail(plan)