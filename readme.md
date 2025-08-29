## 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

  ### getElementById
    It will return a single object with given id. When we have one of a kind object, we decleard them by id and to access them we use getElementById.

  ### getElementsByClassName
    It will return all objects with given class. When we have some objects that will be use on same kind of things, we decleard them by name and to access them all together we use getElementsByClassName. 

  ### querySelector
    It will return the first object with given selector. It searchs all type of selectors such as id, class, name, attributes.  

  ### querySelectorAll
    It will return all the object with given selector. It searchs all type of selectors such as id, class, name, attributes.  

## 2. How to create and insert a new element into the DOM?

  ### create
    We can create a new elemet by using document.createElement().

    This will create a new div:
    const card = document.createElement("div");

    To set id we can do this:
    card.id = "cardLast";

  ### insert
    We can insert a new elemet by using append(), prepend(), insertBefore() and other methods.

    This will get a existing container:
    const parentElement = document.getElementById("cardSet");

    This will add cardLast at then end of cardSet:
    parentElement.appendChild(cardLast);

## 3. What is Event Bubbling and how does it work?

    When an event starts at a specific element and then propagates through its parent and ancestor elements until it reaches the document's root.

    Clicking a button inside a div will firstly trigger buttons handler, then the div, then main, then body and so on.

## 4. What is Event Delegation? Why is it useful?

    When we attch a single event listener in the parent node instead of all child, it is called event delegation.

    When we add child element after the page have been loaded, event delegation can handle them.

## 5. Difference between preventDefault() and stopPropagation()

    preventDefault() stops a browsers default behavior attached with a specific element. When we want to stop the browser from reloading when we submit a form, we can use this.

    topPropagation() stops propagating in bubbling. When we have a event listener at a div and also in a button on the div, clicking on the button will trigger both listener. So we can call stopPropagation() to stop one listener.
