# Ex03 To-Do List using JavaScript
## Date:25/03/2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

### Index.html:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="todo-container">
        <h2>To-Do List</h2>
        <div class="input-section">
            <input type="text" id="todo-input" placeholder="Enter a task...">
            <button onclick="addTask()">Add</button>
        </div>
        <ul id="task-list"></ul>
    </div>
    <script src="script.js"></script>
</body>
</html>
```
### style.css:
```
body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #9f87f6;
    margin: 0;
}

.todo-container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 300px;
}

.input-section {
    display: flex;
    justify-content: space-between;
    margin-bottom: 15px;
}

input {
    flex: 1;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    padding: 8px 12px;
    border: none;
    background: #28a745;
    color: white;
    cursor: pointer;
    border-radius: 5px;
    margin-left: 5px;
}

button:hover {
    background: #218838;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    background: #f59ef5;
    padding: 10px;
    margin: 5px 0;
    display: flex;
    justify-content: space-between;
    border-radius: 5px;
}

.delete-btn {
    background: red;
    color: white;
    border: none;
    padding: 5px 10px;
    cursor: pointer;
    border-radius: 5px;
}

.delete-btn:hover {
    background: darkred;
}

```
### script.js:
```
function addTask() {
    let taskInput = document.getElementById("todo-input");
    let taskList = document.getElementById("task-list");

    if (taskInput.value.trim() === "") {
        alert("Please enter a task!");
        return;
    }

    let li = document.createElement("li");
    li.textContent = taskInput.value;

    let deleteBtn = document.createElement("button");
    deleteBtn.textContent = "X";
    deleteBtn.className = "delete-btn";
    deleteBtn.onclick = function () {
        taskList.removeChild(li);
    };

    li.appendChild(deleteBtn);
    taskList.appendChild(li);
    taskInput.value = "";
}
```

## OUTPUT:

![3](https://github.com/user-attachments/assets/cb859d1c-4dae-4818-850a-8699970890c8)



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
