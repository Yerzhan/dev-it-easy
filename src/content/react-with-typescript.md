---
layout: post
title: 'React with Typescript'
author: [DevIT]
tags: ['React']
image: img/react/reactTypescript.jpg
date: '2020-08-10T11:00:00.00Z'
draft: false
hideinner: true
excerpt: Learn how to start using Typescript with React and what benefits it provides in this simple but very useful tutorial.
---
>TypeScript is an open-source language which builds on JavaScript, one of the world’s most used tools, by adding static type definitions.

Types provide a way to describe the shape of an object, providing better documentation, and allowing TypeScript to validate that your code is working correctly.

Writing types can be optional in TypeScript, because type inference allows you to get a lot of power without writing additional code.

### How to add Typescript support to React application?

One of the simplest ways to start is using [create-react-app](https://create-react-app.dev/docs/adding-typescript/) template and it will create a boilerplate project with everything set up and ready to use.
We just gonna need to execute this example command:

```JS
npx create-react-app my-app --template typescript
# or
yarn create react-app my-app --template typescript
```

The generated project has the same structure as normal one, but instead of _js.config_ file you have _ts.config_ with some compiler options requred to compile the project.

And you can see **tsx** extension which you gonna need to use for components with react markup. It's like **jsx** in React version. If you don't need React you can write Typescript code in files with **ts** extension.

**Watch the video with examples on YouTube**:
`youtube: https://www.youtube.com/watch?v=aVyyzQnWrYI`
