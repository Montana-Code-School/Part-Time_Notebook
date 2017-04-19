# Tuesday, April 17th

Today we are beginning our introduction into React.JS, a library for building user interfaces using Javascript.

* Standup (:5)
* Improv (:5)
    * Categorical Thinking (Exploder)
* We need to begin checking and using Slack more regularly. Some of us still haven’t interacted much on the part time class Slack channel, and the class needs to stay actively engaged in that channel.
* We need to begin utilizing standup and retro more effectively.
* ReactJS
    * Introduction
        * React is a library that we will be using for building user interfaces using JavaScript.
        * React is component based. This means that we can reuse elements of our DOM structure, reducing clutter and allowing for the application to scale well.
        * React also uses what they call the Virtual DOM. This allows React to render the DOM behind the scenes, bypassing some of the inefficiencies that arise while manipulating the DOM manually.
    * Reusable Code / Component Driven Code
        * Once again, we come to the programmers axiom: If you can help it, don’t do the same thing twice.
        * Think of an HTML page. Can you categorize things that you see?
            * Maybe there are some panels, a few menus, maybe there is some sort of different widget on each page. These can each be simplified into reusable chunks. You could create panels, and those panels might all have different information in them. You could create a menu component, with each instance of it having different, unique attributes.
    * State
        * State is a term that you will hear often while working with React.
        * Some of our DOM must be expected to change, especially as we begin developing more single page applications (SPAs), that have more things happening on one page.
        * Stateless vs Stateful
            * If something is stateless, it is immutable. It is not prone to changing, nor is it implied that it is possible to change. It is defined, and remains the way that it was created.
            * If something is stateful, it is apt to change. Maybe some data will be altered when an event occurs. It’s state has changed.
    * Dependencies
        * JSX
            * JSX is a JavaScript preprocessor (it transforms what you write into valid JS) that allows you to write XML-like syntax within React. It essentially will make it easier to read and allows you to use markup that looks a lot like HTML.
        * Babel
            * Babel is a transpiler, allowing us to write our JavaScript using some of the new features present in ECMAScript 6 (ES6, or es2015). This syntax is not currently allowed in all browsers, so we use Babel to transpile our new ES6 code into the previous version of JavaScript.
* Now, we can begin creating our first site using React.js.
    * First, lets take a look at a popular website.
        * What might you reduce down to “components”?
        * What might those props look like?
    * Now, lets recreate some of that. For that I will do some live coding, but the video I have created at https://youtu.be/0HBXCXLoeqA will provide a walkthrough away from class.


## ReactJS
React is a framework created by Facebook that is meant to facilitate component-based, declarative, user interface building.

React alone is not a full framework, it only handles the creation of markup (HTML). This is why we use it in conjunction with other technologies within NodeJS, because a full app cannot be created with React alone.

## JSX
JSX is preprocessor, allowing you to write XML-like syntax within React. This lends to easier readability (remember, XML has a very similar appearance to HTML). It is an optional, but highly recommended approach to writing elegant React code.

## Props
*Props* are how a component is configured. These are immutable properties of a component (although in some circumstances, they are changed dynamically based on relationships with other components, see: http://stackoverflow.com/questions/27991366/what-is-the-difference-between-state-and-props-in-react)

## State
When a component has data that is apt to change often, you will want to use *state*.

## Declarative Programming
Declarative programming is a style in which the logic of a computation is described without having to fully explain it's control flow.

It is concerned with *what* computations should be performed, not *how* those computations should be executed.
