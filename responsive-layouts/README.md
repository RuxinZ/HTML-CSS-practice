# Conquering Responsive Layouts

## Course Summary

In February 2023, I followed the course [Conquering Responsive Layouts](https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts) by Kevin Powell. This is a 21-day course with daily challenges to learn how to create responsive websites, and it's aimed at beginners. The course consists of short videos, and challenges to help you solidify what you have learned.

The course is set up in a way that prevents you from just binge-watching and forgetting everything later. Course content is revealed on a 24-hour interval and solutions are not provided immidiately. You will get a daily email reminder when new course content is unlocked.

The quality of the content is great, and the challenges make sure you understand and practice what you have learned during the video lectures.

Overall, if you're looking to learn responsive web design, this course is definitely worth checking out!

## Table of contents

- [Day 1 Use percentages & avoid heights](#day-1--use-percentages--avoid-heights)
- [Day 2 Get Familiar with relative units](#day-2--get-familiar-with-relative-units)
- [Day 3 Enter max-width](#day-3--enter-max-width)
- [Day 5 Practice Time](#day-5-practice-time)
- [Day 6 Review](#day-6-review)
- [Day 7 Solution to Challenge 3](#day-7-solution-to-challenge-3)
- [Day 8 Flexbox Basics](#day-8-flexbox-basics)
- [Day 9 A deeper dive into flexbox](#day-9-a-deeper-dive-into-flexbox)
- [Day 11 Using flexbox for a navigation](#day-11-using-flexbox-for-a-navigation)

## Day 1 | Use percentages & avoid heights

### Notes-01

1. It’s a good idea to **avoid heights**. HTML is responsive by nature. Use padding if you need more backgroun. If you find your elements not responsive, it's probably caused by some codes in your css file.
2. Percentage on a child element is the percentage of its parent
3. `em` and `rem`:
   - `rem`: root element's font-size
     - best suited for font-size
   - `em`: parent element's font-size
     - best suited for padding, margin, box-shadow, etc.

### [Challenge-01](./challenge-01/)

Change the starter files so that:

- Text only comes to midpoint of the page
- Text does not overflow on bottom on smaller screens

## Day 2 | Get familiar with relative units

No challenge today.

### Notes-02 - `em` vs `rem`

- `em` - a CSS unit relative to the font size of the **parent element**.
  - when used to set spacing, 1em is equal to the font-size of the element itself.
- `rem` - a CSS unit relative to the font size of an **html(root) element**.
  - use rem for font-size
- for _consistent spacing_, use `rem` for padding/margin.
- if you want your padding to adjust based on the element's font-size, for example for a button, use `rem` for the font-size and `em` for padding.

## Day 3 | Enter max-width

### Notes-03

Set a `max-width` with a fixed px value for text contents so that they do not expand too wide on the screen.

### [Challenge-02](./challenge-02/)

- At the moment the text goes from left to right across the whole page --> align text of the header and body on the left.
- Background color of the header should span the entire width of the page.
- The width of text for both the header and body should stop to increase after reaching a certain point.

## Day 4 | Extra curricular activities

## Day 5 Practice time!

### [Challenge-03](./challenge-03/)

There's no starting files for this challenge. Build a webpage with a heading, paragraph, button and background as shown in the example.</br>
</br>
<img src="./challenge-03/design-specs.png " width="600" >

## Day 6 Review

### Note-06

In this first week, we've looked at:

- Using percentages for widths
- Avoiding to set heights
- Using max-width

## Day 7 Solution to challenge #3

### Note-07

- Remember to do CSS reset
- use `margin-inline:auto` to center container
- Default display for button elements if inline-block
- **BEM naming convention in CSS** - Block Element Modifier
  - blockName -> a block itself
  - blockName\_\_itemName -> An element inside the block
  - blockName--modifierName -> modifies the block itself

## Day 8 Flexbox Basics

### Note-08

- `flex-direction` is `row` by default.
- `display:flex` turns the element into a flex container. And the items within it are flex items.
- **flex-items** by default want to be as small as they possibly can be.
- Two different ways to create space in between columns:
  - use `gap` (currently only supported by Firefox)
  - use **Combinator** and `margin-inline-start`
  ```
  .col + .col {
    margin-inline-start: : 1rem;
  }
  ```

### [Flexbox challenge #1](./flexbox-challenge-01/)

1. Make a two-column section.
2. Change the heading color in the middle section
3. center the text and add gaps in between columns

## Day 9 A deeper dive into flexbox

### Note-09

- Use a div container for setting background-color, color, and padding. Within it use a `container` to set the width, max-width, margin-inline(center the text)
- Use different classes for `container` and flexbox `row` to keep them seperate.
- If the text only takes up a certain percentage width of the container, nest another container within it for that.
- Create resuable classes.<br>

**Adding image**

- In a flexbox row, by default all column contents are stretched/shrinked to fit the height of the row. To add an image in the same row with text and avoid streching:
  - Solution 1. Use a div to wrap the image.
  - Solution 2. Give the image a class and add `align-self: flex-start`.<br>

**Column Width and Flexbox**

- `justify-content`
  - alignment for x axis.
  - flexbox by default has `flex-start`.
  - `space-between` takes all spaces and put them in between items

**Ensuring the image is responsive**

- If we used a div to wrap the image in a flexbox. The image itself is not a flex-item anymore. At certain large screen sizes, it might overflow/side-scroll. To solve that, when starting a CSS file, always set `img` to `max-width:100%`.

### [Flexbox challenge #2](./flexbox-challenge-02/)

## Day 11 Using flexbox for a navigation

### Note-11

- In CSS, try to select by class instead of element, except for very generic styling.
- Use semantic elements when possible: `<aside>` for sidebar, `<article>`, etc.
- With the width of columns inside a flexbox row sum up to less than 100% and justify-content on the row set to space-between, it's going to create than gap between the columns automatically.
- When we make something display flex, it's going to try to shrink down to its smallest possible size.
- use `white-space: nowrap;` to prevent text from wrapping when the screen size gets smaller.

### [Flexbox challenge #3](./flexbox-challenge-03/)

Create a header navigation bar

## Day 12 Getting fancy with navigations

### Note-12

- **2 Ways to push some of the items in a navbar to the right:**
  1. Add a class to the first item to be pushed to the right. Set margin-left to auto -> push it all the way to the right
  2. Use 2 nav lists, use flexbox and justify-content: space-between on their parient nav class.
- **Alignment in flexbox:**
  - `justify content` - main axis; `align-items` - cross axis.
- **Adding Logo in header**
  - DO NOT put logo in the nav list if there is a "home" in nav list. It's redundant for screen reader.
  - Set width of nav class to 100% so that it will try to stretch to fit the width as much as it can (pushing the left part to the logo).
