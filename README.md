# React Notes - Daily observations 

-> React code written in a "declarative way"!

In React, writing code in a declarative way means describing what you want the user interface to look like based on the current state, rather than imperatively specifying the step-by-step instructions for how to achieve that state. In other words, you focus on declaring what the UI should be like, and React takes care of updating the UI to match that declaration.

Here are a few key aspects of writing React code in a declarative manner:

State-based: React encourages you to think in terms of state and how it affects the UI. You define the state of your application and how it should be rendered based on that state.

Component-based: React promotes breaking down the UI into reusable components. Each component encapsulates its own state and logic, making it easier to reason about and compose larger UIs.

Virtual DOM: React uses a virtual representation of the actual DOM. When the state of a component changes, React calculates the difference between the previous and new virtual DOM representations and efficiently updates the real DOM to reflect those changes.

Single source of truth: In React, the state is typically managed by a single source of truth, usually stored in a parent component and passed down to child components as props. This ensures that the UI remains consistent and predictable.

By adopting a declarative approach, React allows you to focus on the desired outcome rather than the low-level implementation details. This leads to more maintainable, predictable, and reusable code, as well as easier debugging and testing.

![image](https://github.com/Rahulnayi04/Notes/assets/112021214/e82f0b51-9458-40ec-8480-557d6e82daa8)
