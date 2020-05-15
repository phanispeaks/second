# FlexBox

**Flex is a set of rules for automatically stretching multiple columns and rows of content across a parent container.It can be used to slice and dice your site UI into a responsive layout with relative ease if you know all the right properties.**

**If an item has no HTML elements its content itself is counted as an item. In many cases it's often basic text, a single word, an image or emojis.**

**You can turn flex items into containers. Items sometimes contain content, not more items. Properties justify-items and justify-content in this case apply to content.**

## display: flex
**To enable Flex box, apply display: flex to your HTML element.**

## flex-direction:
**You can define the directional flow of items within their parent container.**
    
### flex-direction: row
**This is the default setting.**

![](https://www.freecodecamp.org/news/content/images/2020/04/image-259.png)

### flex-direction: row-reverse
**But... row-reverse will place the first item at flex-end and invert the order of items:**

![](https://www.freecodecamp.org/news/content/images/2020/04/image-305.png)

### flex-direction: column
**To make items flow down the column change the value of flex-direction to column:**

![](https://www.freecodecamp.org/news/content/images/2020/04/image-260.png)

### flex-direction: column-reverse
**There is also flex-direction: column-reverse. You can guess what it does:**

![](https://www.freecodecamp.org/news/content/images/2020/04/image-311.png)

## Multiple Items
**If you just keep adding items, flex will automatically resize them based on the relative size of all items - even if items were originally set to a height and width. In this example they were set to width=125px and height=125px but notice that they got squeezed:**

![](https://www.freecodecamp.org/news/content/images/2020/04/image-306.png)

## flex-wrap: wrap
**If you want the items to "drop" to the next row add flex-wrap: wrap**

![](https://www.freecodecamp.org/news/content/images/2020/04/image-307.png)

## justify-content
**It defines the alignment along the main axis. It helps distribute extra free space leftover when either all the flex items on a line are inflexible, or are flexible but have reached their maximum size. It also exerts some control over the alignment of items when they overflow the line.**

### justify-content: flex-start

![](https://www.freecodecamp.org/news/content/images/2020/04/image-285.png)

### justify-content: space-between

![](https://www.freecodecamp.org/news/content/images/2020/04/image-286.png)

### justify-content: space-around

![](https://www.freecodecamp.org/news/content/images/2020/04/image-287.png)

### justify-content: space-evenly

![](https://www.freecodecamp.org/news/content/images/2020/04/image-288.png)

### justify-content: center

![](https://www.freecodecamp.org/news/content/images/2020/04/image-289.png)

### justify-content: flex-end

![](https://www.freecodecamp.org/news/content/images/2020/04/image-290.png)
