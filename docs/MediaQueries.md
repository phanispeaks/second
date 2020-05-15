# CSS Media Queries: Breakpoints, Media Types, Standard Resolutions, and More
**In the past, building a website was much simpler. Today a website’s layout should adapt itself not only to computers, but also tablets, mobile devices, and even TVs.**

**Making a website with an adaptable layout is called Responsive Web Design. And CSS Media Queries are one of the most important parts of Responsive Design. In this article, we are going to take a closer look at Media Queries and how to use them in CSS.**

## What is a Media Query?
**A Media query is a CSS3 feature that makes a webpage adapt its layout to different screen sizes and media types.**

### Syntax
```css
@media media type and (condition: breakpoint) {
  // CSS rules
}
```

**We can target different media types under a variety of conditions. If the condition and/or media types meet, then the rules inside the media query will be applied, otherwise, they won’t.**

**The syntax may seem complicated at the beginning, so let’s explain each part one by one in detail…**

## @ Media Rule
We **start defining media queries with @media rule and later include CSS rules inside the curly braces. The @ media rule is also used to specify target media types.**

```css
@media () {
  // CSS rules
}
```

## Parenthesis
**Inside the parenthesis, we set a condition. For example, I want to apply a larger font size for mobile devices. To do that, we need to set a maximum width which checks the width of a device:**

```css
.text {
  font-size: 14px;
}

@media (max-width: 480px) {
  .text {
    font-size: 16px;
  }
}
```

**Normally, the text size will be 14px. However since we applied a media query, it will change to 16px when a device has a maximum width of 480px or less.**

**Important: Always put your media queries at the end of your CSS file.**

## Media Types
**If we don’t apply a media type, the @ media rule selects all types of devices by default. Otherwise, Media types come right after the @ media rule. There are many kinds of devices but we can group them into 4 categories:**

1. all — for all media types
2. print — for printers
3. screen — for computer screens, tablets and, smart-phones
4. speech — for screen readers that “read” the page out loud
