# Conquering Responsive Layouts

A 21-day [course](https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts) by Kevin Powell

## Day 1 | Use Percentages & avoid heights

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
