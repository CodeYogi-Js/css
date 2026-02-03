# CSS Notes

## What is CSS?

CSS stands for **Cascading Style Sheets**.
It describes how HTML elements are to be displayed on the screen, on paper, or in other media.

---

## Creation & Maintenance of CSS

CSS was created by a group of individuals known as the **World Wide Web Consortium (W3C)**.
Primary contributors include **Håkon Wium Lie** and **Bert Bos**.

CSS standards and specifications are maintained by the **W3C**.
A community of web developers, designers, and browser vendors also contributes to its evolution.

Regular updates and new versions ensure CSS remains relevant and adaptable to changing web design needs.

---

## History of CSS Versions

* **CSS1 (1996)**
  Limited properties and selectors.

* **CSS2 (1998)**
  Expanded features; later development toward CSS3 began.

* **CSS2.1 (2011)**
  Fixed errors found in CSS2 and improved stability.

---

## CSS Syntax

A CSS rule consists of a **selector** and a **declaration block**.

```
h1 {
  color: blue;
  font-size: 12px;
}
```

* **Selector** → `h1`
* **Property** → `color`, `font-size`
* **Value** → `blue`, `12px`
* **Declarations** → `color: blue; font-size: 12px;`

---

## CSS Selectors

CSS selectors are used to **find (or select)** the HTML elements you want to style.

### Types of CSS Selectors

We can divide CSS selectors into **five categories**.

## Simple Selectors

### 1. Element Selector

The CSS **element selector** selects HTML elements based on the element name.

```
p {
  text-align: center;
  color: red;
}
```

---

### 2. ID Selector

The **ID selector** uses the `id` attribute of an HTML element to select a specific element.
An ID must be **unique** within a page.

```
#para1 {
  text-align: center;
  color: red;
}
```

---

### 3. Class Selector

The **class selector** selects HTML elements with a specific class attribute.

```
.center {
  text-align: center;
  color: red;
}
```

Example usage:

```
p.center
```

---

### 4. Universal Selector

The **universal selector (`*`)** selects **all HTML elements** on the page.

```
* {
  text-align: center;
  color: blue;
}
```

---
Nice, continuing exactly the same way 👍
Below is the **clean, corrected, README.md-style text** from this image.
Same meaning, **grammar + spelling fixed**, **no new theory added**.

---

## 5. Group Selector

The **group selector** targets multiple elements at once.

```
h1, h2, p {
  color: red;
  text-align: center;
}
```

Styles all `h1`, `h2`, and `p` elements.


## Combinator Selectors

CSS **combinator selectors** are used to define relationships between elements.
They help in selecting elements based on their position and relationship with other elements.

---

### 1. Descendant Selector (space)

* Selects all nested elements inside another element.
* It works even if elements are deeply nested.

**Example:**

```
div p {
  color: blue;
}
```

Selects all `<p>` elements inside `<div>`, even if deeply nested.

**HTML Structure Example:**

```
<div>
  <p>First paragraph</p>
  <section>
    <p>Nested paragraph</p>
  </section>
</div>
```

All `<p>` elements inside `<div>` are affected, no matter how deep they are.

---

### 2. Child Selector (`>`)

* Selects only **direct children** of a parent element.
* Ignores deeply nested elements.

**Example:**

```
div > p {
  color: red;
}
```

* Selects `<p>` elements that are **direct children** of `<div>`.
* Nested `<p>` elements inside other elements are ignored.

Only direct children are affected inside the parent element.

---
Perfect, continuing 👍
Below is the **clean, corrected, README.md-style text** from this page.
Same meaning, **grammar + spelling fixed**, **no extra theory added**.

---

### 3. Adjacent Sibling Selector (`+`)

The **adjacent sibling selector** selects the **immediate next sibling** of an element.
Only the **first next element** is affected.

If the condition is repeated multiple times, it is checked step by step and applied accordingly.

**HTML Example:**

```
<h1>Title</h1>
<p>First paragraph</p>   <!-- applied -->
<p>Second paragraph</p>  <!-- not applied -->
```

---

### 4. General Sibling Selector (`~`)

The **general sibling selector** selects **all sibling elements** that come **after** a specified element.

**Example HTML:**

```
<h1>Title</h1>
<p>First paragraph</p>     <!-- applied -->
<div>Some content</div>
<p>Second paragraph</p>    <!-- applied -->
```

**CSS:**

```
h1 ~ p {
  color: green;
}
```

Selects all `<p>` elements that appear **after `<h1>`**, even if other elements are in between.

##  Pseudo-class Selectors

As of **CSS3 and CSS4**, there are **45+ pseudo-class selectors**.
Pseudo-classes help style elements based on **user interaction**, **structure**, **form states**, and more.

---

### Link States & User Interaction

* `:hover`
* `:focus`
* `:active`
* `:link`
* `:visited`

---

### Structure & Position Based

* `:first-child`
* `:last-child`
* `:nth-child(n)`
* `:nth-last-child(n)`
* `:first-of-type`
* `:last-of-type`
* `:nth-of-type(n)`
* `:only-child`
* `:only-of-type`
* `:empty`

## Form & Input States

* `:checked`
* `:disabled`
* `:enabled`
* `:required`
* `:optional`
* `:read-only`
* `:read-write`
* `:valid`
* `:invalid`
* `:placeholder-shown`

## UI & Selection

* `:target`
* `:checked`
* `:selection`

---

## Advanced CSS4 Selectors

* `:is()`
* `:where()`
* `:has()`

## Link Pseudo-classes (Anchor States)

Link pseudo-classes allow styling based on the **state of a link**, depending on user interaction.

* `:link` → link not yet visited
* `:visited` → link already visited
* `:hover` → mouse pointer over the link
* `:focus` → link selected via keyboard or click
* `:active` → link being clicked

### Order of Link Pseudo-classes (LVHFA)

The order of link pseudo-classes **must be followed** due to CSS specificity rules:

```
:link → :visited → :hover → :focus → :active
```

## Focus Pseudo-class

The `:focus` pseudo-class is used to target elements when the user interacts with them using the keyboard or mouse.

This selector works on **user input elements**, commonly used in forms.

---

## Example

```
input:focus {
  background-color: black;
  color: white;
}
```

**HTML Example:**

```
<form>
  <p>
    <input name="first" />
  </p>
  <p>
    <input name="last" />
  </p>
</form>
```

### `:focus-within`

Targets an element **when any of its child elements is focused**.

* Used mainly on **parent containers**
* Applies when input fields inside the container get focus

**Example:**

If a container has an input field and you focus on that input, the **parent container** gets the styles applied.

---

### `:focus-visible`

Targets an element **only when focus is visible**, usually via **keyboard navigation**.

* Improves accessibility
* Avoids showing focus styles on mouse clicks
* Useful for keyboard users

---

## `:target` Pseudo-class

The `:target` pseudo-class is used to style an element **when it is targeted by a URL fragment** (hash `#`).

* Works with anchor links
* Highlights the element when navigated to

**Use case:**

Clicking a link that points to a specific section highlights that section.


## Example: `:target`

Imagine a page with multiple sections.

When you click a link like:

```
Go to Section 1
```

The browser jumps to that section, and the targeted element gets styled.

**CSS Example:**

```
:target {
  border: 2px solid red;
  background-color: beige;
}
```

---

## HTML Example

```
<p><a href="#section1">Jump to New Content 1</a></p>
<p><a href="#section2">Jump to New Content 2</a></p>

<p id="section1">New Content 1</p>
<p id="section2">New Content 2</p>
```

* Clicking the link jumps to the section
* The targeted section gets highlighted
* Style applies only to the active target

---

## Summary

* `:focus-within` → parent reacts when child is focused
* `:focus-visible` → focus shown only when appropriate
* `:target` → styles applied when element is targeted via URL

---










