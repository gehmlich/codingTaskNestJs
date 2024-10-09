# BayWa Coding Task Backend

## Task definition

Develop a REST API endpoint for a “Task” entity with the following properties: id, title, description, status, and createdAt. The endpoint should support the full CRUD operations (Create, Read, Update, Delete). Alternatively, you can choose your own entity with five properties.

## Objective

The endpoint should successfully execute all CRUD operations for the selected entity. Functioning data validation is required and simple unit tests must be implemented. The task is successfully completed when the CRUD functionality is complete, the validation works correctly and the unit tests pass.

### Test criteria

- The CRUD operations are implemented correctly and work as expected.
- Input data is checked using class-validator.
- The code contains at least one unit test per CRUD operation that passes.


## Implementation steps

1. Resource selection:    

- Select a simple resource, such as Task, Note or User.
- Define which fields the resource should have (e.g. id, title, description, createdAt for a task resource).

2. Module creation:
  
- Create a new module for the resource (nest g module tasks).

3. Create service and controller:

- Create a service and controller for the resource (nest g service tasks and nest g controller tasks).
- Implement the basic CRUD endpoints in the controller:
  - GET /tasks: Returns all tasks.
  - GET /tasks/:id: Returns a task by ID.
  - POST /tasks: Adds a new task.
  - PUT /tasks/:id: Updates an existing task.
  - DELETE /tasks/:id: Deletes a task.
 
4. Data model and validation:

- Define a DTO (Data Transfer Object) for the resource, e.g. CreateTaskDto and UpdateTaskDto.
- Use class-validator to ensure that the input data is correct (e.g. @IsString(), @IsNotEmpty()).

5. Implement the logic in the service:

- Implement the logic for the CRUD operations in the TasksService.
- Use a simple in-memory data structure (e.g. an array) to temporarily store the data.

6 Testing and evaluation:

- Test the endpoints with a tool such as Postman or Swagger
- Discuss afterwards:
  - How the modules and dependencies are structured.
  - Which additional features would be possible (e.g. authentication).
  - Optimization options for larger data volumes or databases.
