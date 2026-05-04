# to-do-app
To-Do App

A simple and interactive To-Do List web application built using HTML, CSS, and JavaScript.
This project allows users to add tasks, mark tasks as completed, and delete tasks dynamically.

Features
Add new tasks
Delete tasks
Mark tasks as completed
Press Enter key to add tasks
Input validation for empty tasks
Simple and clean user interface
Technologies Used
HTML5
CSS3
JavaScript (DOM Manipulation)
Project Structure
project-folder/
│
├── index.html
├── todostyle.css
└── README.md
How It Works
1. Add Task
Type a task inside the input field.
Click the ADD button or press Enter.
The task will appear in the task list.
2. Complete Task
Click on the task text.
The task will toggle between completed and uncompleted states.
3. Delete Task
Click the ❌ button beside a task.
The task will be removed from the list.
JavaScript Functionalities
DOM Selection
const input=document.getElementById("taskInput");
const add=document.getElementById("addBtn");
const list=document.getElementById("taskList");

These lines select the input field, add button, and task list from the HTML document.

Event Listeners
add.addEventListener("click",addtask);

Runs the addtask() function when the ADD button is clicked.

input.addEventListener("keypress",function(e){
if(e.key==="Enter"){
  addtask();
};
});

Allows users to press the Enter key to add a task.

Task Validation
if(task===""){
    alert("invalid input");
    return;
}

Prevents empty tasks from being added.

Creating Elements Dynamically
const span=document.createElement("span");
const btndel=document.createElement("span");
const li=document.createElement("li");

Creates task elements dynamically using JavaScript.

Mark Task as Completed
span.addEventListener("click",function(){
  span.classList.toggle("completed");
});

Toggles the completed CSS class when a task is clicked.

Delete Task
btndel.addEventListener("click",function(){
  li.remove();
});

Removes the selected task from the list.

Future Improvements
Save tasks using Local Storage
Add edit functionality
Add task deadlines
Dark mode support
Responsive mobile design
