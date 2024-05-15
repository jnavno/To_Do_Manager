# Task Manager Application

This Java project implements a task manager that utilizes a priority queue mechanism to manage and prioritize tasks based on their due times. The backbone of the priority queue is a custom-built heap data structure, specifically tailored to manage objects that require comparison based on time priority.
This project was built without any java library.

## Features

- **Custom Heap Implementation**: A generic heap data structure that extends Java's `Comparable` interface, allowing for the comparison and management of custom task objects.
- **Priority Queue**: A simple priority queue wrapper around the heap to facilitate task management operations like insertion and retrieval based on priority.
- **Task Management**: Ability to manage tasks with specific due times, leveraging Java's `LocalTime` to handle time comparisons.

## Components

1. **Heap**: Generic class for the heap implementation, supporting basic operations like insert, removeMax, and automatic resizing.
2. **PriorityQueue**: Wrapper class that utilizes the `Heap` for storing tasks and managing them based on their urgency.
3. **Task**: Represents a task with a due time and a description. It includes methods for comparing tasks and retrieving due time.

## Usage

Here's how you can use this application:

```java
PriorityQueue<Task> todo = new PriorityQueue<>();

todo.insert(new Task(LocalTime.of(9, 00), "Leave for work"));
todo.insert(new Task(LocalTime.of(11, 30), "Meeting with tutor"));
todo.insert(new Task(LocalTime.of(10, 00), "Call bank"));
todo.insert(new Task(LocalTime.of(16, 00), "Finish essay"));
todo.insert(new Task(LocalTime.of(13, 00), "Remember lunch"));

// Display the next task
System.out.println("Next task is: " + todo.takeNext());
```

## Installation
To run this project, you will need a Java development environment set up with JDK 11 or later. Clone this repository, compile the Java files, and execute the main method in the Task class to see it in action.

## Contributions
Contributions are welcome. Please fork this repository and submit a pull request if you have something to add or modify.

## License
Distributed under the MIT License. See LICENSE for more information.
