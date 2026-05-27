# AirBnB Clone - The Console

## Description

This project is the first step toward building a full web application that clones AirBnB.
It includes a command interpreter to manage the objects of the project, a storage engine using JSON, and several data models.

The command interpreter allows you to:
- Create new objects (User, Place, etc.)
- Retrieve objects from a file
- Update attributes of an object
- Destroy an object
- List all objects or objects by class

## The Command Interpreter

### How to Start

**Interactive mode:**

```
$ ./console.py
(hbnb)
```

**Non-interactive mode:**

```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  all  create  destroy  help  quit  show  update

(hbnb)
```

### How to Use

Type commands at the `(hbnb)` prompt.

**Commands:**

- `create <class>` - Creates a new instance and prints the id
- `show <class> <id>` - Prints the string representation of an instance
- `destroy <class> <id>` - Deletes an instance
- `all [class]` - Prints all instances, or all of a given class
- `update <class> <id> <attribute> <value>` - Updates an attribute of an instance
- `quit` - Exit the program
- `EOF` - Exit the program (Ctrl+D)
- `help` - Show available commands

**Supported classes:** BaseModel, User, State, City, Amenity, Place, Review

### Examples

```
$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'id': '49faff9a-6318-451f-87b6-910505c55907', ...}
(hbnb) all BaseModel
["[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {...}"]
(hbnb) update BaseModel 49faff9a-6318-451f-87b6-910505c55907 first_name "Betty"
(hbnb) destroy BaseModel 49faff9a-6318-451f-87b6-910505c55907
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
** no instance found **
(hbnb) quit
$
```

## Authors

See the [AUTHORS](./AUTHORS) file.
