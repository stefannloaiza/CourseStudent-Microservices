
# Students and Courses Microservices

Server-side application using microservices architecture to manage courses and students and their relationships. The application is made with Java 17 and has an implementation of:

- Eureka (Eureka server and feign client)
- Spring config server
- Lombok

## API Reference

### Students

#### Get all students

```http
  GET /api/student/all
```

#### Get student by id

```http
  GET /api/student/search/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `int` | **Required**. Id of student to search |


#### Get all students by course id

```http
  GET /api/student/search/${courseId}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `courseId`      | `int` | **Required**. Id of the course to search all their students |


#### Save new student

```http
  POST /api/student/create
```

| Request Body | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `student`      | `Student` | **Required**. Student object to create |


### Courses

#### Get all courses

```http
  GET /api/course/all
```

#### Get courses by id

```http
  GET /api/course/search/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `int` | **Required**. Id of course to search |


#### Get all students by course id

```http
  GET /api/course/search-student/${courseId}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `courseId`      | `int` | **Required**. Id of the course to search all their students |


#### Save new course

```http
  POST /api/course/create
```

| Request Body | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `course`      | `Course` | **Required**. Course object to create |

## Authors

- Stefann Loaiza - [@stefannloaiza](https://www.github.com/stefannloaiza)

