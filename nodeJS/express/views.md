### Introduction

We’ll need a way of rendering the data from our controller functions, and views let do that. In the context of the MVC architecture, views are the user-facing part of the application. They are the UI that the user interacts with. Views are sections of code that generate the HTML for our applications. They define the layout for the rendered HTML and allow data to be rendered where dictated in our layout.

We use template engines to create our views. More specifically, template engines are used to create template files that transform the template into HTML. Any variables defined in our template files are replaced with actual data.

In this course, we will use [EJS](link: https://ejs.co/) which lets us write in JavaScript to create HTML markup.

### Lesson overview

This section contains a general overview of topics that you will learn in this lesson.

- EJS Installation
- EJS Syntax
- Application of EJS

### Setting up EJS

Let's get started with EJS! Install EJS into your application by typing the following into your terminal:

```bash
npm install ejs
```

At the root of your project, create a subfolder called `views`.

Next, we need to let our app know that we intend to use `EJS` as a template engine, as well as where to look for view files.

In your `app.js` file, add the following:

```js
app.set("views", path, join(__dirname, "views"));
app.set("view engine", "ejs");
```

This enables `EJS` as the view engine, and that our app should look for templates in the `/views` subdirectory.

### Template syntax

In `EJS`, the `<%` and `%>` tags allow us to use JavaScript. Whatever is in these tags will behave like JavaScript. This lets us write conditional statements, `for` loops, and use variables.

In order to work with variables, we use the `<%=` tag. This lets us convert variables into values when the application is loaded. Otherwise, stick with `<%` when using JavaScript logic.

Here's a quick example that makes includes arrays and loop logic.

```js
<% const animals = ["Cat", "Dog", "Lemur", "Hawk"];%>

<% animals.map(animal => {%>
- <%= animal%>s are cute <% }) %>
```

#### Note box variations

<div class="lesson-note" markdown="1">

#### A sample title

A sample note box.

</div>

<div class="lesson-note lesson-note--tip" markdown="1">

#### level 4 heading for title is recommended

A sample note box, variation: tip.

</div>

<div class="lesson-note lesson-note--warning" markdown="1">

#### But title is also optional

A sample note box, variation: warning.

</div>

<div class="lesson-note lesson-note--critical" markdown="1">

A sample note box, variation: critical.

</div>

### Assignment

<div class="lesson-content__panel" markdown="1">

1. A RESOURCE ITEM
   - AN INSTRUCTION ITEM
1. A PRACTICE ITEM
   - A TASK ITEM

</div>

### Knowledge check

The following questions are an opportunity to reflect on key topics in this lesson. If you can't answer a question, click on it to review the material, but keep in mind you are not expected to memorize or master this knowledge.

- [A KNOWLEDGE CHECK QUESTION](A-KNOWLEDGE-CHECK-URL)

### Additional resources

This section contains helpful links to related content. It isn't required, so consider it supplemental.

- It looks like this lesson doesn't have any additional resources yet. Help us expand this section by contributing to our curriculum.