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
#### When using em for sizes for fonts we are referencing the font size of it's parent element and this size is compounding 
#### When using em for margin and padding and all other elements not font we are referencing the font size of that element 
#### Question, about how many pixels is 5em? It would typically be 5 x your parent element's font size and so if your parent's font is 16px then 5em will be 80px (5 x 16px)
#### The browser default is 16px font size and so 1em is generally 16px -- relative to the parent element and within available media-query 
#### rem is always looking at the root font size and so it is more consistent 
#### rem is useful to keep margins consistent sizes 
#### em is useful padding and margin 
#### it is also best practice to use rem for font sizes due the compounding nature of em
#### once a media-query is added to the html element then rem will reference that provided font size of that media-query 
## CSS Tip #3 
### Utilize vw for big title font sizes for responsive titles it will allow for less media queries 
#### vh, vw, vmax, vmin reference and ratio the viewport 
#### it doesn't work too well with paragraph text 
#### vmax for height can be useful when you want to prevent an image from blowing too big 
#### lots of extensive testing when using these units 

