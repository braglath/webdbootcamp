below will be the comments for css

####### FONTS #####

px -- is the most commonly used unit
but not recommended for responsive website as it will be changing

font-size to change the size of the font

changing font, fonts should be installed in the browser
safe to use the browser fonts
https://www.cssfontstack.com/ check the link for commonly used fonts
you can add many fonts as choices one after another by adding a comma

text transform to uppercase/lowecase/capitalize in css

use mark{} in css to change the color of the marker

HELLO THERE
how are you doing???

testing git push for the second time

###### CSS SELECTOR

Universal Selector - _ - this selects everything in the document
example
_{
color:black;
} - this makes everything black

button - this selects all buttons
example
button{
font-size: 18px;
}

we can use comma to use multiple selectors
like
h1,h2{
font-size: violet;
}

###### ID Selector

we can use id to hook between html and css
but when using an id of a html in css, you have to add #in front of the id in css
no space between # and the id text in css
1 id should be only used once when for the hook
use id selectors as less as possible, there are other selectors to style individual elements

##### Class Selector

same as an id selector(check above) but this can be use on multiple elements
when using class hook in css, you have to add a . in front of the class name in css
by using class we can group together different elements to style them in css

###### Decendant Selector

we write using a space
decendants - like we have in list, one inside another

####### Adjacent selector ######
we write using +
adding two selectors **(one selector which is right inside another)** to style
but only the second selector will be styled
example
h1 + P {
color:red;
}
above, h1 is a selector and p is another selector and we add them by putting + inbetween

###### Direct Child

selects only the li that are directly inside a div
example
div > li{
color:white;
}

#### Attribute Selector

select an input element where the type attribute is set to "text"
example
input[type="text"]{
width: 300px;
color: yellow;
}

class of post
section[class="post"]{
color:blue;
}

href matching
a[href="www.google.com"]{
color=blue;
}

href containing
a[href*="example"]{
font-size\*=2px;
}

href ending
a[href$=".org"]{
font-style:italic;
}

######## Pseudo Class ######
they all start with a collon
keyword added to a selector that specifies a special state of the selected element(s)
:active - currently on active( style when the element press and hold)
:checked - radio button or checkboxes
:first
:first-child
:hover - style when the cursor is hovering on the element
:not()
:nth-child()
:nth-of-type(3) - style the 3rd element
:nth-of-type(3n) - style every 3rd element

###### Pseudo Elements

they all start with ::
keyword added to a selector that lets you style a particular part of selected element(s)
::after - add stylized text at the end of a line, not only text we can also have special charcs, icons, url and more
z::first-letter - stylize the first letter of an element
::selection - when a user selects something on the page, you can stylize the color and more

###### The CSS Cascade

the order your styles are declared and linked matters!!!!!!!!
whatever style comes the second wins
example
h1{
color:blue;
}
h2{
color:purple;
}
from the above style, only the purple color will be shown!!!!!
this also matters even when we use more than one style sheet
the order we link the css in main html file also matters. whatever comes second will be shown
overrides the first style

###### Specificity

it is how the browser decides which rules to apply when multiple rules could apply to the same element
it is a measure of how specific a given selector is. The more specific selector "wins"
oder of Specificity
ID, Class, Element
we can use "specifitycalculator.com"

if you add "!important" at the end of any style then it wins \
generally try not to use important as it only overrides and it is not the right way

inline styles - styling a element inside of css in the same line
generally avoid inline style as it makes more confusing

##### Inheritance

elements will get the style even if it is not directly applied
example
HTML

<body>
<h1>sdfsdfsdsd</h1>
</body>

CSS
body{
color:blue;
}

certain elements don't inherit styles by default
all texts will inherit

workaround to inherit a color
button{
color: inherit;
}

######### Box ##########
width - width of the entire box, this alters the contents inside the box
height - height of the entire box, this alters the contents inside the box
border-width - thickness of the border
border-color - color of the border
border-style - line style , dashed, solid and more

##### Padding

spacing on the inside of the border
same as above we can add padding to individual sides
examples of usages
padding: 10px; - put padding on all 4 sides
padding: 5px 10px; - padding on verical and horizontal sides
padding: 1px 3px 2px; - top | horizontal | bottom
padding: 5px 1px 0 3px; - top | right | bottom | left

### Margin

spacing on the outside of the border
just like others we have all 4 individual properties - left, right, bottom, top
examples of usages
margin: 10px; - put padding on all 4 sides
margin: 5px 10px; - padding on verical and horizontal sides
margin: 1px 3px 2px; - top | horizontal | bottom
margin: 5px 1px 0 3px; - top | right | bottom | left

#### Display Property

display: inline;

inline element - width and height are ignored. Margin & padding push elements away horizontally
but not vertically
block - break the flow of a document. Width, height, margin & padding are respected.
inline-block - behave like an inline element except Width, height , margin & padding are respected

examples
h1 takes up entire line of space
span does not take up entire line of space

#### CSS Unites

Relative Units
em, rem, vh, vm, %
example
width: 50% - half the width of the parent
line-height: 50% - half the font size of the element itself

em- 1em = font-size of the parent.
2em = twice the font size of the parent
and so on
ems are so useful in buttons and varying sizes
ems completely depends on the parent font size
problem with ems are they can grow or shrink quickly so only choose ems when there is only one parent
we can use rems for the problem above

rems - same as ems 1x 2x and so on but it only considers the root element's size

Absolute Units - px

###### Opacity and Alpha Channel

rgba(red,gree,blue,alpha)
alpha value is 0-1
either give a color value of rgba or opacity:
example - color: rgba(255,255,255,1); - color with opacity
or opacity: 1; - only opacity

if an opacity is applied to a parent then all the elements/contents within that parent will also get affected

#### Position

top, right, bottom and left values
we can also use negative values (-100px)

static - noting affects and the element position will not be changed
example
position:static;
top: 100px;

relative - space is given as if position were static but this offsets the position relative to the document/line/container
example
position: relative;
right: 100px;
object moves left (offsets)

fixed - removed from the document flow, no space is given and no offset
**\***very useful for nav bar**\*\***
example
position: fixed;
top: 100px;

absolute - removed from the flow of the document and no space is given like relative
this also brings the element in front of other elements
example
position: absolute;
top: 5px;
if the parent has a position of relative then the element with position absolute will only move inside the parent

sticky - not fixed when scrolling but fixed when the scroll comes back to the position
**\*\*\*\*** very useful for nav bar **\*\*\***

-webkit-sticky - check in MDN website

###### Transitions

transitions: 1s;
transition from one to another , like when hover
we can add the transition to the main element, not needed on hover style
we can specify property name, duration, timing function and delay

specific property name -
transition: background-colour 1s;

for all properties -
transition: all 1s;

delay-
transition: background-colour 2s 1s; here 1s is the delay and 2s is the transition time

we can also add multiple transitions in a single line but putting a comma
example
transition: border-width 2s, background-color 1s;

Timing Function
there are many transition timing functions that are built in
transition-timing-function: ease-in
ease-out
liner
and more
go to easings.net for bounce and more ease anime codes

######## Transform ####
for a block level element if the margin is set to be auto then it will come to the center of the screen
use transfotm-origin to pin the rotation
example
transform-origin: top left;
matrix, matrix3d
perspective
rotate, rotate3d - deg, grad, turns
example-
transform: rotate(360deg);
transform: rotate3d(360deg);
transform: rotatex(360deg);
y
z

translate, translate3d - to move an element, we also have translate3d, translate x y and z
have to be a length or some percentage
example-
transform: translatex(100px);

scale, scale3d - same as rotate, this will scale the element, we also have scale3d, scale x y and z
example-
transform: scale(2);
transform: scale(xaxis,yaxis);

skew, skewx, skewy - accepts angles(deg), skews an element

##### BUTTON HOVER ANIMATION

box-shadow: 12px 12px 10px 10px red; - xaxis, yaxis, blur radius, spread radius, color
text-shadow: 12px 12px 10px 10px red; - xaxis, yaxis, blur radius, spread radius, color
cursor: pointer; - changes the cursor to a pointer(like a hand clicking button)

#### BACKGROUND

background-image:url(paste the url or the file location path here);
we can also have multiple background

background-size: cover/contain/auto/<length>/<percentage>;
contain - scales the image and it will repeat the image if any empty spaces. this will not crop or stretch the image
cover - scales the image, it stretches the image to fill up
auto - scales the image in such a way that the image's proportions are not changed
we can also use units and also give 2values like x and y
background-size: 3em 25%;

background-repeat: repeat-x/repeat/space/round/no-repeat/space repeat;
repeats are best for patterns

background-position: top/left/center/ 25% 75%/bottom 50px right 100px/

background - this is the property that sets all the other background property in a single line - order generally does't matter
but if we want to add background size then we need to add / right after the position property
background-clip/background-color/background-image/background-origin/background-position/background-repeat/background-size and background-attachment

##### Google Fonts

mostly use the fonts that are in google
fonts.google.com
you can just download the font or copy the embed and paste it in the <head> section of our html
check the paring section to see what two fonts go well with each other
copy and past the style css code from the website
font-family: Raleway, sans-serif;

## **Calculations**

calc();
code example
margin: calc(10%/6);

### Problem with Html

automatically provides a spaces inbetween
<img>
<img>
when the code is in different line then it creates a space inbetween
if using flex boxes then this issue will be addressed

# **Flex Box**

# **flex-direction**

<flex-direction: row;>
_puts the element inside a flex-box in a row(one next to another)_

<flex-direction: row-reverse;>
_puts the element inside a flex-box in a row but reverse the elements_

<flex-direction: column;>
_puts the element inside a flex-box in a column(one below another)_

<flex-direction: column-reverse;>
_puts the element inside a flex-box in a column but reverse the elements_

# **justify-content**

_how to elements of a flex-box is distributed_

- <justify-content: flex-start;>
  _if our main axis if from left to right then this will put the elements at the start_

- <justify-content: flex-end;>
  _this will put the elements at the end(opp of flex-start)_

- <justify-content: center;>
  _this will center our elements along the main axis_

- <justify-content: space-between;>
  _create equal spaces between the adjacent elements but not outside the elements_

- <justify-content: space-around;>
  _create space around the elements(opp of space-between)_

- <justify-content: space-evenly;>
  _create equal/even spaces around the elements(best to use than space-around)_

# **Flex Wrap**

**when the flex box size is smaller than the elements inside, then the flex box will reduce the size of the elements inside it**

_how the elements inside a flex-box are wrapped_

- <flex-wrap: wrap;>

  - _puts the elements inside without changing the size of the elements(then we can use justify-content to determine the spaces between the elements)_
  - _wraps downwards_

- <flex-wrap: wrap-reverse;>

  - _ (opp of wrap)puts the elements inside without changing the size of the elements but reverses the elements (then we can use justify-content to determine the spaces between the elements)_
  - _wraps upwards_

  - <flex-wrap: nowrap;>

  - _no wraps(nothing happens)_