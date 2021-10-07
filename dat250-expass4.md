# DAT250: Software Technology Experiment Assignment 4

## Code

- Code is [here](https://github.com/andlekbra/dat250-expass4-rest-todo)


## Setup
- REST Api for todos implemented using Spark and MongoDB for storage
- Trying out VS Code Devcontianer to have more control of the development environment and avoid installing dependencies in host system
- The app is running in a vscode devcontainer. The mongodb is running in a separate container

## Progress
- Created project with vs code java extension template
- Added devcontainer files
- added docker-compose to set up mongodb container and docker network
- Used code from [Spark/Java red-green-counter example](https://github.com/selabhvl/dat250-sparkjava-counter) as a starting point
- Implemented CRUD functionality for todos

## Functionality
### Json representation of Todo object

```json
{
  "_id": {
    "$oid": "615a015933a4f4442a6130e1"
  },
  "summary": "Something to do",
  "description": "describing the thing to do"
}

```

### Operations

All operation done on `localhost:8080/todos`

#### POST

- Body must contain a valid todo item in json.
- Summary cannot be empty.
- Will create a todo item and persist in database

#### GET
- `localhost:8080/todos` will get all todos
- `localhost:8080/todos/<identification>` will return the specific todo

#### PUT

- `localhost:8080/todos/<identification>` and a valid todo object in the body will update the todo item.

#### Delete

- `localhost:8080/todos/<identification>` will remove the todo item


## Problems
- Had problems with the Java language support from VS code when running in devcontainer. Found help [here](https://github.com/redhat-developer/vscode-java/issues/743). Problem seemed to be caused by lombok extension installation. Java extension where trying to open lombok extension but lombok was not available in the devcontainer.