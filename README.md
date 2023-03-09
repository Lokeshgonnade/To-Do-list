# To-Do-list


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Todo List</title>
    <style>
        .container{
            margin: auto;
            padding: 15px;
            border: 2px solid black;
            height: 300px;
            width: 300px;
        }
        #task{
            padding: 10px;
    
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Add your To do list here </h1>
        <div id="newtask">
            <input type="text" placeholder="Add Tasks">
            <button id="push">Add</button>
        </div>
        <h2>To Do List</h2>
        <div id="tasks"></div>
    </div>

    <script>
        document.querySelector('#push').onclick = function(){
    if(document.querySelector('#newtask input').value.length == 0){
        alert("Kindly Enter Task Name!!!!")
    }

    else{
        document.querySelector('#tasks').innerHTML += `
            <div class="task">
                <span id="taskname">
                    ${document.querySelector('#newtask input').value}
                </span>
                <button class="delete">
                    delete
                </button>
            </div>
        `;

        var current_tasks = document.querySelectorAll(".delete");
        for(var i=0; i<current_tasks.length; i++){
            current_tasks[i].onclick = function(){
                this.parentNode.remove();
            }
        }
    }
}
    </script>
</body>
</html>
