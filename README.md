# Responsive-Layouts with CSS - Tips and Tricks
## CSS Tip #1 
### Avoid using height in most scenarios, especially fixed heights:
#### The web is naturally responsive, when you start adding height in your CSS you are essentially taking away that responsiveness
#### Utilize padding to control the size of your spacing instead of adding height
### It is best to use Percentages rather than fixed widths to make our lives easier:
#### Keep in mind it is the percentage of its parent element width and the most parent element is the viewport 
#### I typically avoid using width with child elements as well when possible
## CSS Tip #2
### With sizes avoid using pixels to keep the responsiveness of the web:
#### When using 'em' for sizes for fonts we are referencing the font size of its parent element and this size is compounding 
#### When using 'em' for margin and padding and all other elements not font we are referencing the font size of that element 
#### Here's a question; how many pixels is 5em? It would typically be 5 x your parent element's font size and so if your parent's font is 16px then 5em will be 80px (5 x 16px)
#### The browser default is 16px font size and so 1em is generally 16px -- relative to the parent element and within available media-query 
### 'rem's will always reference the root font size and so it is more consistent 
#### 'rem's are useful to keep margins consistent in sizes 
#### em is useful padding 
### It is best practice to use 'rem's for font sizes due to the compounding nature of em
#### Once a media-query is added to the html element then the 'rem's will reference that provided font size of that media-query 
## CSS Tip #3 
### Utilize vw for large title font sizes for responsive titles. It will allow for less media queries 
#### vh, vw, vmax, vmin reference and ratio the viewport 
#### these units do not work too well with paragraph font sizes
#### vmax for height can be useful when you want to prevent an image from blowing up too big 
#### ensure lots of extensive testing when using these units 
## CSS Tip #4
### Don't use 'em's for font-size, but rather use 'rem's
#### Remember em's are compounding building on the element's font-size 
#### 'rem's reference the root font-size which is typically 16px for most browsers 
## CSS Tip #5
### Flex items will want to shrink down to the size of its elements and so set width to 100%
#### Because of this nature Flex elements may lead to side-scrolling 
### Note the following CSS code:
#### .col + .col {}
#### if a column has an adjacent sibling column it will be selected 
#### in other words, if the col has something before it then it will be selected 
#### to acquire the gap result (as gap{} is only available in Firefox) we can do the following:
#### .col + .col {
####    margin-left: 32px; 
#### }
## CSS Tip #6
### Combine class names such as 'container' and 'row' 
#### 'container' class will handle the padding and margins of most sections and the 'row' class will handle the display flex 
#### HTML: <div class="container row"></div>
#### CSS: container{ margin: 2rem } row{display: flex}
## CSS Tip #7
### Set all img tags to max-width: 100% within its div to ensure images will not overflow
#### In the parent div of your img tag, utilize align-self: flex-start to keep alignment to the top
#### .hero__img {
####    align-self: flex-start;
#### }
## CSS Tip #8 
### In a flex container of a row of elements, say a nav bar, you can differentiate the margin of one or more elements by utilizing 'margin-left: auto'. This will move the targeted items to the very right of the area    
#### Do note flex justify-content space between is one of the more useful flex attributes 
## CSS Tip #9 
### With @media queries min-width and max-width, the meanings are actually the opposite
#### E.g. @media (min-width: 600px){} //this means 600px or bigger
#### E.g. @media (max-width: 600px){} //this means 600px or smaller
### @media (minx-width: 600px) and (max-width: 900px) {} // here we are targeting (inclusive) between 600px and 900px 
### In your CSS file the order to which @media (min-width: ) is place is very crucial. Anything lower in the file overrides the top, and so you must place your @media queries from smallest to biggest 
## CSS Tip #10
### Which breakpoints should I use? See below
### Use the following media query breakpoints: 600px, 900px, 1200px, and 1800px
#### For SASS utilize the following at your discretion: 
#### @mixin for-phone-only {
####   @media (max-width: 599px) { @content; }
#### }
#### @mixin for-tablet-portrait-up {
####   @media (min-width: 600px) { @content; }
#### }
#### @mixin for-tablet-landscape-up {
####   @media (min-width: 900px) { @content; }
#### }
#### @mixin for-desktop-up {
####   @media (min-width: 1200px) { @content; }
#### }
#### @mixin for-big-desktop-up {
####   @media (min-width: 1800px) { @content; }
#### }
## CSS Tip #11
### Typography goes a long way 
### Utilize text CSS properties "line-height" and "letter-spacing" 
## CSS Tip #12
### CSS Custom properties are variable CSS properties you can reuse 
### You can define custom properties in the root 
### :root {
### --primary-color: purple; 
### }
### body {
### color: var(--primary-color)
### }






