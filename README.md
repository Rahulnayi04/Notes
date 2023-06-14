# React Notes - Daily observations 

# React code written in a "declarative way"!

In React, writing code in a declarative way means describing what you want the user interface to look like based on the current state, rather than imperatively specifying the step-by-step instructions for how to achieve that state. In other words, you focus on declaring what the UI should be like, and React takes care of updating the UI to match that declaration.

Here are a few key aspects of writing React code in a declarative manner:

State-based: React encourages you to think in terms of state and how it affects the UI. You define the state of your application and how it should be rendered based on that state.

Component-based: React promotes breaking down the UI into reusable components. Each component encapsulates its own state and logic, making it easier to reason about and compose larger UIs.

Virtual DOM: React uses a virtual representation of the actual DOM. When the state of a component changes, React calculates the difference between the previous and new virtual DOM representations and efficiently updates the real DOM to reflect those changes.

Single source of truth: In React, the state is typically managed by a single source of truth, usually stored in a parent component and passed down to child components as props. This ensures that the UI remains consistent and predictable.

By adopting a declarative approach, React allows you to focus on the desired outcome rather than the low-level implementation details. This leads to more maintainable, predictable, and reusable code, as well as easier debugging and testing.

![image](https://github.com/Rahulnayi04/Notes/assets/112021214/e82f0b51-9458-40ec-8480-557d6e82daa8)


# Introducing JSX

JSX (JavaScript XML) is an extension to the JavaScript language syntax used in React. It allows you to write HTML-like code within JavaScript, making it easier and more intuitive to define the structure and appearance of React components.

Here are some key points about JSX:

Syntax: JSX resembles HTML syntax, but it is not actual HTML. It is a syntactic sugar that gets transformed into regular JavaScript function calls during the compilation process. JSX elements look similar to HTML tags but are actually function calls that create React elements.

Embedding expressions: JSX allows you to embed JavaScript expressions within curly braces {}. This means you can include variables, function calls, or any JavaScript expression directly within JSX elements. For example, {name} could be used to render the value of a variable named name.

Components: JSX supports the creation and rendering of React components. You can use custom component names as if they were HTML tags. For example, <MyComponent /> represents the usage of a custom React component named MyComponent.

Attributes: JSX supports passing props (properties) to components using HTML-like attributes. These attributes get transformed into props objects that are passed as arguments to the component. For example, <MyComponent color="blue" /> passes the color prop with a value of "blue" to the MyComponent component.

Self-closing tags: Just like in HTML, JSX allows you to use self-closing tags for elements without children. For example, <img src="image.jpg" alt="description" />.

Conditional rendering: JSX allows you to conditionally render elements or components using JavaScript expressions. You can use ternary operators, logical operators, or even if statements within curly braces to conditionally render different parts of the JSX code.

JSX is not required to use React, but it is commonly used because it provides a concise and readable way to define the structure and behavior of React components. Under the hood, JSX is transformed into regular JavaScript function calls that create and update the React components.

# Why Componenets 

![image](https://github.com/Rahulnayi04/Notes/assets/112021214/23eac32c-3099-41f3-bec0-9a2524d03673)
 
# Passing data via "props"

![image](https://github.com/Rahulnayi04/Notes/assets/112021214/b92826fc-2ec3-4878-a5b1-905fc0c8af4d)

# Concept of "Composition" ( children props )
---------------------------------------------

# User Interaction And State

# Working with "STATE"

In React, the useState hook is used to manage state within functional components. The useState hook allows you to declare a state variable and provides a function to update that variable. Here's an example of how to use the useState hook in a React component:


# Here's An example code 
**import React, { useState } from 'react';

function Counter() {
  // Declare a state variable called "count" and its updater function "setCount"
  const [count, setCount] = useState(0);

  // Event handler to increment the count
  const incrementCount = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={incrementCount}>Increment</button>
    </div>
  );
}**

# Controlled vs Uncontrolled Components

Components can be classified as controlled or uncontrolled based on how they manage and update their state.
**1. Controlled Components:**
Controlled components are those where the component's state is fully controlled by the parent component. The parent component passes the current state values to the controlled component as props, and the controlled component notifies the parent when changes occur through callback functions. The parent component has full control over the data flow and handles the updates to the component's state.

Benefits of controlled components:

The parent component has complete control over the component's state and can enforce validation or business logic before updating the state.
Easy to test and reason about since the state is explicitly managed by the parent component.
Enables sharing and synchronization of state between multiple components.

Example of a controlled component:

**function ControlledInput(props) {
  return (
    <input
      value={props.value}
      onChange={props.onChange}
    />
  );
}**

**2. Uncontrolled Components:**
Uncontrolled components, on the other hand, manage their own state internally, without relying on the parent component to control their state. The component maintains its state using a ref or other internal mechanisms and updates its state independently. The parent component does not have direct control over the state of an uncontrolled component.

Benefits of uncontrolled components:

Simplifies the code as there is no need for callbacks or state management in the parent component.
Suitable for simple forms or inputs where real-time updates or validation are not required.
Can be faster for large forms since there is no need for re-rendering when the component's state changes.

Example of an uncontrolled component:


# Understanding "keys"

When rendering a list of elements in React, the key prop is a special attribute that helps React identify individual elements and efficiently update and re-render them when the list changes.

The key prop is required when rendering a list of elements using the **map()** function or any other method that generates multiple components dynamically. It should be assigned a unique identifier for each item in the list. React uses these keys to keep track of elements and optimize the rendering process.

Here are a few important points to understand about keys in React:

**Uniqueness:** Each key within a list should be unique among its siblings. React uses keys to determine which elements have changed, been added, or been removed. Using unique keys allows React to efficiently update only the elements that have changed.

**Stable Identity:** The key prop should be based on an attribute or property of the list items that remains stable across renders. Using index as a key is generally not recommended, as it may cause issues when the list order changes or items are added or removed.

**Reconciliation:** When the list is updated, React compares the new list with the previous one and performs a process called reconciliation. It matches elements with the same keys and updates them, adds new elements, and removes elements that no longer exist. Having stable and unique keys helps React accurately determine which elements have changed.

**Performance:** Using appropriate keys can significantly improve the performance of rendering lists in React. When a list item's key changes, React treats it as a new item and re-renders it from scratch. On the other hand, if a key remains the same, React can optimize by reusing the existing component without re-rendering it entirely.

**Example: **







