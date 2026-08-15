# Simple JavaScript Todo App

A lightweight, interactive To-Do List application built using core web technologies. This project demonstrates basic DOM manipulation, dynamic element creation, and efficient event handling in Vanilla JavaScript.

## 🚀 Features
* **Add Tasks:** Dynamically insert new items into your to-do list.
* **Delete Tasks:** Remove completed or unwanted tasks instantly.
* **Input Auto-Clear:** The input field resets automatically after a task is added.
* **Event Delegation:** Uses a single event listener on the parent list (`<ul>`) to handle deletions for both existing and newly created tasks efficiently.

## 🛠️ Tech Stack
* **HTML5:** Structures the app's user interface.
* **CSS3:** Adds custom background colors and visual layout blocks.
* **JavaScript (ES6):** Handles the core application logic and dynamic interactivity.

## 📦 Project Structure
Make sure your local directory is organized like this for the code to run correctly:
├── index.html
├── style.css
└── mini.js

## 💻 How to Run This Project
1. **Clone or Download** this repository to your local machine.
2. Open the project folder.
3. Double-click the **`index.html`** file to launch the application directly in any web browser.

## 📜 Key Code Insights
Instead of adding individual event listeners to every single delete button (which fails for newly added tasks), this project uses **Event Delegation**:
```javascript:-
ul.addEventListener("click", function(event){
    if(event.target.nodeName == "BUTTON"){
        let listItem = event.target.parentElement;
        listItem.remove();
    }
});
```
This listens for clicks on the entire `<ul>` element and accurately targets the specific delete button clicked, ensuring even freshly generated tasks can be deleted flawlessly.
