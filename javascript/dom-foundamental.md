HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vanilla JS List App</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; background: #f4f4f4; }
    ul { list-style: none; padding: 0; }
    li { padding: 5px 10px; background: white; margin-bottom: 5px; cursor: pointer; }
    li.completed { text-decoration: line-through; color: gray; }
    input { padding: 5px; margin-right: 5px; }
    button { padding: 5px 10px; }
  </style>
</head>
<body>
  <h1>Vanilla JS Task List</h1>

  <input type="text" id="taskInput" placeholder="New task...">
  <button id="addBtn">Add Task</button>

  <input type="text" id="filterInput" placeholder="Filter tasks...">

  <ul id="taskList"></ul>

  <script src="app.js"></script>
</body>
</html>

JavaScript (app.js)
// --- DATA ---
let tasks = []; // this array stores your tasks

// --- DOM ELEMENTS ---
const taskInput = document.getElementById("taskInput");
const addBtn = document.getElementById("addBtn");
const filterInput = document.getElementById("filterInput");
const taskList = document.getElementById("taskList");

// --- FUNCTIONS ---

// Renders the UI based on tasks array and optional filter
function render(filter = "") {
  taskList.innerHTML = ""; // clear list

  tasks
    .filter(task => task.text.toLowerCase().includes(filter.toLowerCase()))
    .forEach((task, index) => {
      const li = document.createElement("li");
      li.textContent = task.text;
      if (task.completed) li.classList.add("completed");

      // Toggle complete on click
      li.addEventListener("click", () => {
        tasks[index].completed = !tasks[index].completed;
        render(filterInput.value); // re-render with current filter
      });

      // Right-click to remove
      li.addEventListener("contextmenu", (e) => {
        e.preventDefault();
        tasks.splice(index, 1);
        render(filterInput.value);
      });

      taskList.appendChild(li);
    });
}

// Add a new task
addBtn.addEventListener("click", () => {
  const text = taskInput.value.trim();
  if (text === "") return;

  tasks.push({ text: text, completed: false });
  taskInput.value = "";
  render(filterInput.value);
});

// Filter tasks as user types
filterInput.addEventListener("input", () => {
  render(filterInput.value);
});

// Initial render
render();

How It Works — Fundamentals Covered

DOM Selection – getElementById, querySelector, querySelectorAll

Event Handling – click, input, contextmenu

Creating/Removing Elements – document.createElement, appendChild, removeChild (via splice + render)

Toggling State – boolean completed stored in array

Filtering – .filter() + .includes()

Data ↔ UI Sync – render() function redraws list from array