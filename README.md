# graph_api
Playing around GraphQL, NodeJS and Express


```sh
mutation updateTopic($id: Int!, $topic: String!) {
  updateCourseTopic(id: $id, topic: $topic) {
    ...courseFields
  }
}


query getCoursesWithFraments($courseID1: Int!, $courseID2: Int!){
  course1: course(id: $courseID1){
    ...courseFields
  }
  course2: course(id: $courseID2){
    ...courseFields
  }  
}

fragment courseFields on Course {
  title,
  author,
  description,
  topic,
  url
}




query getSingleCourse($courseId: Int!){
  course(id: $courseId) {
    title,
    author,
    description,
    topic,
    url
  }
}

query getCoursesByTopic($topic: String){
  courses(topic: $topic) {
    title,
    author,
    description,
    topic,
    url
  }
}
```