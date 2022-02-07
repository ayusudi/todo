# Command Line Application with Javascript 

## TODO ASYNC 

### Class 

Class ToDo 
- id : number
- task : string
- status : string
- created_at : date
- completed_at : date 
- remaining_time (private) : number
- tags : [] (default)

Class ToDoCompleted
- id : number
- task : string
- status :  "completed"
- created_at : date
- completed_at : date 
- remaining_time (private) : 0
- tags : [] (default)

Class ToDoUncomplete
- id : number
- task : string
- status :  "uncomplete"
- created_at : date
- completed_at : null 
- remaining_time (private) : number
- tags : [] (default)

Class Tag 
- name : string

Create Factory Method for ToDo  

### Create Read Create & Update to Completed

```
$ node app.js 
$ node app.js add <task> <remaining_time>
$ node app.js completed <todo id>
```

## READ 

> $ node app.js 
```bash
List ToDo :

[
   ToDoCompleted {
        "id": 1, 
        "task": "Review Perbuddy",
        "status": "uncompleted",
        "created_at": "",
        "completed_at": null,
        "remaining_time": 1,
        "tags": [
            Tag { name : "H8" }, 
            Tag { name  : "MVC" }, 
            Tag { name : "OOP" }
        ]
    },
    ToDoUncomplete {
        "id": 2, 
        "task": "Take a Bath",
        "status": "completed",
        "created_at": "",
        "completed_at": "",
        "remaining_time": 0,
        "tags": [
            Tag { name : "Life" },
            Tag { name : "Clean" }
        ]
    }
]
```


## Create 

> $ node app.js add 'Belajar MVC' 3

```
Success create ToDo "Belajar MVC" with remaining time 3 days. 
```

## UPDATE COMPLETED

> $ node app.js completed 3
```
Complete task id 3 with nama "Belajar MVC" now remaining time is 0 days.
```