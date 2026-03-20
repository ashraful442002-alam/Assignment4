1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?


Answer: Difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll

getElementById → returns one element or null – fastest
getElementsByClassName → returns live HTMLCollection of elements with that class
querySelector→ returns first matching element (or null)
querySelectorAll → returns static NodeList of all matching elements


2. How do you create and insert a new element into the DOM?
Answer: 

const newDiv = document.createElement('div');
newDiv.textContent = "Hello, I am a new div!";
newDiv.className = "my-new-div";

// Insert it into the DOM
document.body.appendChild(newDiv); 

3. What is Event Bubbling? And how does it work?
Answer:Event Bubbling is the process where an event starts from the deepest target element and bubbles up through its ancestors in the DOM tree until it reaches the root
<div id="parent">
  <button id="child">Click Me</button>
</div>

document.getElementById('parent').addEventListener('click', () => {
  console.log('Parent clicked');
});

document.getElementById('child').addEventListener('click', () => {
  console.log('Child clicked');
});

4. What is Event Delegation in JavaScript? Why is it useful?
Answer: Event Delegation: You put one event listener on a parent element and check event.target to see which child was clicked.

It is Usefull for:
Reduces memory usage by attaching fewer listeners.

5. What is the difference between preventDefault() and stopPropagation() methods?
Answer: preventDefault() stops the browser’s default action (like following a link), while stopPropagation() stops the event from bubbling up to parent elements.

