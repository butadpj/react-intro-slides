---
theme: default
title: The history
class: text-left
transition: slide-left
---

### index.html
___

```js {*}{maxHeight:'60vh'}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="design.css" />
    <title>Todo App</title>
  </head>

  <body>
    <div class="app">
      <header>Todo App</header>
      <br />
      <form class="todo-form">
        <input class="todo__input" type="text" placeholder="Add your new todo" />
        <button type="submit" class="add-btn btn">Add</button>
      </form>
      <ul class="todo__list">
        <!-- 
          <li>
              Some todo 
              <div>
                <button class="btn done-btn">Done</button> 
                <button class="btn delete-btn">Delete</button>
              </div>
          </li> 
        -->
      </ul>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

---
theme: default
title: The history
class: text-left
transition: slide-left
---

### index.html
___

```js {7}{maxHeight:'60vh'}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="design.css" />
    <title>Todo App</title>
  </head>

  <body>
    <div class="app">
      <header>Todo App</header>
      <br />
      <form class="todo-form">
        <input class="todo__input" type="text" placeholder="Add your new todo" />
        <button type="submit" class="add-btn btn">Add</button>
      </form>
      <ul class="todo__list">
        <!-- 
          <li>
              Some todo 
              <div>
                <button class="btn done-btn">Done</button> 
                <button class="btn delete-btn">Delete</button>
              </div>
          </li> 
        -->
      </ul>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

---
theme: default
title: The history
class: text-left
transition: slide-left
---

### index.html
___

```js {31}{maxHeight:'60vh'}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="design.css" />
    <title>Todo App</title>
  </head>

  <body>
    <div class="app">
      <header>Todo App</header>
      <br />
      <form class="todo-form">
        <input class="todo__input" type="text" placeholder="Add your new todo" />
        <button type="submit" class="add-btn btn">Add</button>
      </form>
      <ul class="todo__list">
        <!-- 
          <li>
              Some todo 
              <div>
                <button class="btn done-btn">Done</button> 
                <button class="btn delete-btn">Delete</button>
              </div>
          </li> 
        -->
      </ul>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

---
theme: default
title: The history
class: text-left
transition: slide-left
---

### design.css
___

```css {*}{maxHeight:'60vh'}
:root {
  --primary: rgb(71, 26, 129);
  --secondary: rgb(80, 62, 163);
  --dark: rgb(24, 23, 23);
  --light: rgb(238, 238, 238);
  --success: rgb(38, 151, 43);
  --danger: rgb(175, 43, 43);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-size: 16px;
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  background: var(--secondary);
}

header {
  font-size: 2em;
  color: var(--light);
  font-weight: 800;
}

.app {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column;
}

.todo-form {
  width: 80%;
  max-width: 25rem;
  display: flex;
  justify-content: space-around;
}

.todo__input {
  width: 100%;
  padding-left: 1em;
  border: none;
}

.todo__input:focus {
  outline: none;
  border:1px solid var(--dark);
}

.todo__list {
  margin-top: 5em;
  width: 80%;
  max-width: 30rem;
  list-style: none;
}

.todo__list li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: var(--light);
  font-size: 1.5em;
  padding: 1em;
}

.todo__list li:hover {
  background: var(--primary);
}

.btn {
  border: none;
  padding: 1em 1.5em;
  color: black;
  cursor: pointer;
}

.btn:hover {
  filter: brightness(120%);
}

.done-btn {
  background: var(--primary);
  color: white;
}

.delete-btn {
  background: var(--danger);
  color: white;
}

.add-btn {
  background: var(--success);
  color: white;
}
```

---
theme: default
title: The history
class: text-left
transition: slide-left
---

### script.js
___

```js {*}{maxHeight:'60vh'}
let input = document.querySelector('form input');
let addBtn = document.querySelector('.add-btn');
let inputValue = ''; 

const resetInput = () => {
  // Reset input value and do focus
  input.value = '';
  inputValue = '';
  input.focus();
};

const todoButtonsEventHandler = (newTodo) => {
  const doneBtn = newTodo.querySelector(".done-btn");
  const deleteBtn = newTodo.querySelector(".delete-btn");
  let isTodoDone = false;

  if (doneBtn) {
    doneBtn.addEventListener('click', () => {
      // If doneBtn with text "Done" is click
      if (!isTodoDone) {
        newTodo.style.textDecoration = 'line-through';
        doneBtn.innerText = 'Undo';
        isTodoDone = true;
      }
      // If doneBtn with text "Undo" is click
      else {
        newTodo.style.textDecoration = 'none';
        doneBtn.innerText = 'Done';
        isTodoDone = false;
      }
    });
  }

  if (deleteBtn) {
    deleteBtn.addEventListener('click', () => {
      // Get the current todo (parent element of the button)
      newTodo.remove();
    });
  }
};

const createElements = () => {
  let todoList = document.querySelector('.todo__list');

  // Create a todo element with a text based on the input value - li
  let newTodo = document.createElement('li');
  newTodo.innerText = `${inputValue} `;

  let buttonsWrapper = document.createElement('div');

  // Create a button element with text "Done"
  let doneBtn = document.createElement('button');
  doneBtn.className = 'done-btn btn';
  doneBtn.innerText = 'Done';

  // Create a button element with text "Delete"
  let deleteBtn = document.createElement('button');
  deleteBtn.className = 'delete-btn btn';
  deleteBtn.innerText = 'Delete';

  todoList.prepend(newTodo);
  buttonsWrapper.appendChild(doneBtn);
  buttonsWrapper.appendChild(deleteBtn);
  newTodo.appendChild(buttonsWrapper);


  todoButtonsEventHandler(newTodo); // Handles todo's "Done/Undo" & "Delete" button 
};

const addTodo = () => {
  if (!inputValue) {
    // If input is empty
    input.focus();
  } else {
    createElements(); // Create the todo and its buttons
    resetInput(); // Reset input value and do focus
  }
};


window.onload = () => {
  addBtn.addEventListener('click', (e) => {
    e.preventDefault(); // Prevent page reload if submit button is pressed
    addTodo();
  });

  input.addEventListener('input', (e) => {
    inputValue = e.target.value;
  });
}
```