# Responsive-Layouts with CSS - Tips and Tricks
## CSS Tip #1 
### Avoid using height in most scenarios:
#### The web is naturally responsive, when you start adding height in your CSS you are essentially taking away that responsiveness
#### Utilize padding to control the size of your spacing instead of adding height
### It is best to use Percentages rather fixed widths to make our lives easier:
#### Keep in mind it is the percentage of it's parent element width and the most parent element is the viewport 
#### I typically avoid using width with child elements as well when possible
## CSS Tip #2
### With sizes avoid using pixels to keep responsiveness of the web:
#### When using 'em' for sizes for fonts we are referencing the font size of it's parent element and this size is compounding 
#### When using 'em' for margin and padding and all other elements not font we are referencing the font size of that element 
#### Question, about how many pixels is 5em? It would typically be 5 x your parent element's font size and so if your parent's font is 16px then 5em will be 80px (5 x 16px)
#### The browser default is 16px font size and so 1em is generally 16px -- relative to the parent element and within available media-query 
### 'rem's will always reference the root font size and so it is more consistent 
#### 'rem's are useful to keep margins consistent sizes 
#### em is useful padding 
### It is best practice to use 'rem's for font sizes due the compounding nature of em
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
### Flex items will want to shrink down to the size of it's elements and so set width to 100%
#### Because of this nature Flex elements may lead to side-scrolling 
### Note the following CSS code:
#### .col + .col {}
#### if a column has an adjacent sibling column they will be selected 
#### in other words if the col has something before it then it will be selected 
#### to acquire the gap result (as gap{} is only available in Firefox) we can do the following:
#### .col + .col {
####    margin-left: 32px; 
#### }
## CSS Tip #6
### Combine classnames such as 'container' and 'row' 
#### 'container' class will handle the padding and margins of most sections and the 'row' class will handle the display flex 
#### HTML: <div class="container row"></div>
#### CSS: container{ margin: 2rem } row{display: flex}
## CSS Tip #7
### Set all img tags to max-width: 100% within it's div to ensure images will not overflow
#### In the parent div of your img tag, utilize align-self: flex-start to keep alignment to the top
#### .hero__img {
####    align-self: flex-start;
#### }


