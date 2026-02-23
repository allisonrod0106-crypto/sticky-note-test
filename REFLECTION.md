# REFLECTION

## Q1 - Reactivity: When you type inside the textarea, the character counter updates automatically. Explain why this happens. (mention v-model, Vue reactivity, and what data property changes)
    The character count updates automatically because of Vue's reactivity system. v-model binds the textarea to a data property which in this case is stickie.text Vue rerenders any part of the template that relies on the property such as (text ?? "").length
## Q2 - Deep Watch: Explain what deep: true does and what would stop working if we removed it. 
    deep: true allows Vue to observe the changes being made inside of an object/array. Without it, persistent localStorage would not work. 
## Q3 - localStorage:
    What type of data does localStorage store? 
        Strings
    Why do we use JSON.stringify() when saving?
        We use JSON.stringify() when saving because arrays and objects cannot be directly stores in localStorage. 
    What would happen if we forgot JSON.parse() when loading?
        If we forgot JSON.parse() the stringified array would be returned and it will be treated as a string. 
## Q4 - Delete Logic: Explain the following:

    What does .filter() return?
        .filter() returns an array with only the items that match the specified condition. 
    Why assign the result back to this.stickies? 
        We reassign the result back to this.stickies because filter returns a new array, so we want to replace the old one with the new one to remove items. 
    Why !== and not ===? 
        !== keeps the items that do not match the id
        === keeps the item that matches the id which is not what we want 

## Q5 - Architecture Decision: Why is saving implemented in a separate method (saveToStorage) instead of writing localStorage code directly in the watcher? 
    Implementing saving in a separate method allows reusuability. It can be used in various places easily without having to duplicate code in every watcher or method. Additionally, it keeps responsibilities organized and separate - the watcher observes changes and the save method handles the data. 
    