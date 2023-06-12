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
import React, { useState } from 'react';

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
}







