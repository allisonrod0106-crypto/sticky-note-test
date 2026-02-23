# AI Use Documentation

PROMPT: How to create an ID object in JS using crypto.randomUUID()?
RESPONSE:
If you want an object with an ID property, you can do:
    const newObject = {
    id: crypto.randomUUID(),
    name: "Sample Item",
    createdAt: new Date()
    };

    console.log(newObject);
WHAT I USED: 
    const newObject = { id: crypto.randomUUID(), text: "Sample Text"};

PROMPT: What does Array.filter() do?
RESPONSE:
    Array.filter() in JavaScript is a method that creates a new array containing only the elements of the original array that pass a certain test condition. It does not modify the original array.
WHAT I USED: 
     this.stickies = this.stickies.filter(sticky => sticky.id !== id);