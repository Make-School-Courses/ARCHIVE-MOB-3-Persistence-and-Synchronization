# Project - Course Planner

Sessions are occurences of Courses.
Course can have many sessions. 
Course Session can have many notes attached.
Courses can have many Projects. Projects can be marked as completed or not. Projects have a due date.

You know how to store trivial information in Core Data. The purpose of this project is for you to develop a professional working applicatin with Core Data. Think about your architectural choices. 

Your code will be examined on these categories:
    - Code modularizaton
    - Commenting Code
    - The use of simple abstractions
    - Use of the Core Data Stack
    - Performance of code
    - Swift style guide & Tools (Protocols, Enums etc)

## Entities
- Course
- Session
    - Belongs to a Course
- Note
    - Belongs to a Session
- Project
    - Belongs to Course
    - Completed property
    - Due Date property

## Requirements

- Use core data to store user's courses, course sessions and notes for each session.
- Read data from the main context and write on a private background context.
- Project reminder; send a local notification a few hours before a project is due.

## UI

The interface is up to you to decide. I have provided a sample design, but you are free to experiment with your own interpretations.


## Extra Challenges

- Share Course Notes from one device to another using bluetooth
- Use a markdown parser to find the course page for each class(on github) and display it as Syllabus.