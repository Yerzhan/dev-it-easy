---
layout: post
title: 'What is React JS? How does React Work?'
author: [DevIT]
tags: ['React']
image: img/react/whatIsReact.jpg
date: '2020-08-15T23:46:37.121Z'
draft: false
hideinner: true
excerpt: Overview of React JS and how does it work under the hood.You will learn about what is React and how does React works. What makes React efficient and how it manipulates the DOM using the virtual DOM concept.
---
**Watch the video with examples on YouTube**:
`youtube: https://www.youtube.com/watch?v=GoUMk3C9Eyc`

**React** is a declarative and efficient JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called **components**.

To understand how React achieves this, we need to learn about **DOM** - The Document Object Model 

When HTML code of the page is parsed by the browser it's turned into DOM. In simplest cases DOM looks like the source HTML of the page and represents the UI of your application, but it usually differs a lot since JavaScript can manipulate the DOM to provide dynamic behavior to the page. 

React also can manipulate the DOM and it uses **ReactDOM.render** function to render elements in the DOM:
```JS
    const element = <h1>Hello, world</h1>;
    ReactDOM.render(element, document.getElementById('root'));
```
But frequent manipulations of the DOM affect performance, making it slow even though the DOM is represented as a tree data structure and changes to the DOM are fast. But after the change, the updated element and its children have to be re-rendered to update the application UI. The re-rendering of the UI makes it slow. Therefore, the more UI components you have, the more expensive the DOM updates could be, since they would need to be re-rendered for every DOM update.

To solve this issue React uses the concept of **virtual DOM** that performs significantly better than the real DOM. 

When new elements are added to the UI, React creates an in-memory data-structure cache which is represented as a tree. Each element is a node on this tree. If the state of any of these elements changes, a new virtual DOM tree is created. This tree is then compared or diffed with the previous virtual DOM tree.
After the difference is found React batch updates the real DOM with the best possible method.
This process is called **reconciliation**.

This selective rendering provides a major performance boost. It saves the effort of recalculating the CSS style, layout for the page, and rendering for the entire page.

>In simple words, you tell React what state you want the UI to be in, and it makes sure that the DOM matches that state. The great benefit here is that as a developer, you would not need to know how the attribute manipulation, event handling or the manual DOM updates happen behind the scenes.

All of these details are abstracted away from React developers. All you need to do is update the states of your component as and when needed and React takes care of the rest. 

That's all for the basics of the React JS.
