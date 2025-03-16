# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
    <link rel="stylesheet" href="index.css">
</head>
<body>
    <header>
        <h1 id="main-heading">Welcome to JavaScript DOM Manipulation</h1>
    </header>

    <main>
        <p id="paragraph">Click the button to change this text and add a new element.</p>

        <button onclick="changeText()">Change Text</button>
        <button onclick="toggleElement()">Add/Remove Element</button>
    </main>

    <div id="container"></div>

    <script src="script.js"></script>
</body>
</html>



function changeText() {
    let paragraph = document.getElementById("paragraph");
    paragraph.textContent = "The text has been changed dynamically!";
    paragraph.style.color = "blue";  
    paragraph.style.fontSize = "18px";
}


function toggleElement() {
    let container = document.getElementById("container");
    let existingElement = document.getElementById("newElement");

    if (existingElement) {
        container.removeChild(existingElement);  
    } else {
        let newElement = document.createElement("p");
        newElement.id = "newElement";
        newElement.textContent = "New element added!";
        newElement.style.color = "green";
        newElement.style.fontWeight = "bold";
        container.appendChild(newElement);
    }
}

body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 20px;
}

button {
    padding: 10px 15px;
    margin: 10px;
    border: none;
    background-color: #007BFF;
    color: white;
    cursor: pointer;
    border-radius: 5px;
}

button:hover {
    background-color: #0056b3;
}

#container {
    margin-top: 20px;
}



