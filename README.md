<!DOCTYPE html>
<html>
<head>
    <title>To-Do List</title>
</head>
<body>
    <h1>To-Do List</h1>
    
    <h2>Pending Tasks</h2>
    <ul id="pendingTasks">
        <li><input type="checkbox"> Task 1</li>
        <li><input type="checkbox"> Task 2</li>
    </ul>

    <h2>Completed Tasks</h2>
    <ul id="completedTasks">
        <li><input type="checkbox" checked> Task 3</li>
    </ul>

    <form>
        <input type="text" id="newTask" placeholder="Add a new task">
        <button type="button" onclick="addTask()">Add</button>
    </form>

    <script>
        function addTask() {
            const newTaskText = document.getElementById("newTask").value;
            if (newTaskText) {
                const pendingTasksList = document.getElementById("pendingTasks");
                const newTask = document.createElement("li");
                newTask.innerHTML = `<input type="checkbox"> ${newTaskText}`;
                pendingTasksList.appendChild(newTask);
                document.getElementById("newTask").value = "";
            }
        }
    </script>
</body>
</html>
