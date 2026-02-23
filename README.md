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