# damn_css

## CSS Color
3 types of decleration 
1. rgb/rgba (red,green,blue,alpha) range: rgb(0->255,0->255,0->255,0->1) decleration: rgba(21,2,40,0.25)
2. Hex #rrggbb range: 00 and ff (same as decimal 0-255) eg: #2cf9c4 and #d20 equivalent to #dd2200
3. HSL/ HSLA(hue, saturation, lightness, alpha) eg: hsla(9, 100%, 64%, 0.2) or hsl(9, 100%, 64%)
  *Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue.
  Saturation is a percentage value, 0% means a shade of gray, and 100% is the full color.
  Lightness is also a percentage, 0% is black, 50% is neither light or dark, 100% is white
  The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all)*

## Setting up background image

```
background: background-color background-image background-repeat background-attachment background-position;
```

#### Backgorund Color and Image
```
  background-image: url /*url('URL')*/
                    none /**default*/
                    initial /*Sets this property to its default value*/
                    inherit /**Inherits this property from its parent element*/
                    linear-gradient(red, yellow)
                    repeating-linear-gradient(rgb)
                    conic-gradient()
                    radial-gradient()
    
  /* Used if the image is unavailable */
  background-color: name_of_color
                    rgba
                    Hex
                    hsl  
```
#### Backgorund Repeat
```
background-repeat: repeat /**default, repeat over both axis x as well as y*/
                   no-repeat 
                   repeat-x /* repeat over x- axis**/
                   repeat-y
                   space	 //down
                   round	  //The background-image is repeated and squished or stretched to fill the space
                   initial // 	Sets this property to its default value
                   inherit
```
*space -> The background-image is repeated as much as possible without clipping. The first and last image is pinned to either side of the element, and whitespace is distributed evenly between the images*

#### Backgorund Attachment
```
background-attachment: //specifies whether the background image should scroll or be fixed (will not scroll with page)
                       fixed // background stays in the same place when scrolling
                       scroll //background moves with the rest of content when scrolling
                       local	//background moves within the local element when the local element's scroll bar is being moved
```
![image](https://user-images.githubusercontent.com/54256549/170739149-2c633075-580e-4a16-85ef-e928df34b6ff.png)

#### Backgorund position
```
background-position: /*sets the starting position of a background image*/
                     left top //default
                     left center
                     left bottom
                     right top
                     right center
                     right bottom
                     center top
                     center center
                     center bottom
                     x% y% //down
                     xpx ypx
                     initial	// Sets this property to its default value
                     inherit	// Inherits this property from its parent element
                     
```
*x% y% -> The first value is the horizontal position and the second value is the vertical. The top left corner is 0% 0%. The right bottom corner is 100% 100%. If you only specify one value, the other value will be 50%. Default value is: 0% 0%*

#### Background Clip
```
background-clip: // defines how far the background (color or image) should extend within an element
                border-box	//default value. The background extends behind the border	
                padding-box	//The background extends to the inside edge of the border	
                content-box	//The background extends to the edge of the content box	
                initial	
                inherit
```

#### Background origin
```
Note: This property has no effect if background-attachment is "fixed".
background-origin: /* specifies the origin position (the background positioning area) of a background image */
                   padding-box	//default value, The background image starts from the upper left corner of the padding edge	
                   border-box	// The background image starts from the upper left corner of the border, padding area will also covered
                   content-box	// The background image starts from the upper left corner of the content	
                   initial	// Sets this property to its default value
                   inherit	// Inherits this property from its parent element. Read about inherit
```

## CSS Bording 

```
border-style: //specifies what kind of border to display
              dotted - Defines a dotted border
              dashed - Defines a dashed border
              solid - Defines a solid border
              double - Defines a double border
              groove - Defines a 3D grooved border. The effect depends on the border-color value
              ridge - Defines a 3D ridged border. The effect depends on the border-color value
              inset - Defines a 3D inset border. The effect depends on the border-color value
              outset - Defines a 3D outset border. The effect depends on the border-color value
              none - Defines no border
              hidden - Defines a hidden border
```

## Margins
*You can set the margin property to auto to horizontally center the element within its container*
```
margin: margin-top margin-right margin-bottom margin-left;

margin: margin-top margin-right and margin-left margin-bottom; e.g margin: 25px 30px 45px

margin: margin-top and margin-bottom  right and left margin;
```

## Padding

```
padding: padding-top padding-right padding-bottom padding-left;

padding: padding-top padding-right and padding-left padding-bottom; e.g padding: 25px 30px 45px

padding: padding-top and padding-bottom  right and left padding;
```
**Note**
*if an element has a specified width, the padding added to that element will be added to the total width of the element. This is often an undesirable result*
exapmle
```
div {
  width: 300px;
  padding: 25px;
}
Here, the <div> element is given a width of 300px.
However, the actual width of the <div> element will be 350px 
(300px + 25px of left padding + 25px of right padding)
```
*To keep the width at 300px, no matter the amount of padding, you can use the box-sizing property. This causes the element to maintain its actual width*
``
box-sizing: border-box;
``
## Links
*a:link - a normal, unvisited link //mostly used to convert text look like links.
a:visited - a link the user has visited
a:hover - a link when the user mouses over it
a:active - a link the moment it is clicked //A link becomes active when you click on it*

*``text-decoration`` property is mostly used to remove underlines*

## Outline

*An outline is a line that is drawn around elements, OUTSIDE the borders, to make the element "stand out"*
```
outline : outline-width outline-style(required) outline-color
```

## Text
*The text-align property is used to set the horizontal alignment of a text*
*The ``vertical-align`` property sets the vertical alignment of an element*

```
text-align: left 
            right 
            centered 
            justified /*stretched so that every line has equal width, and the left and right margins are straight (like in magazines and newspapers)*/

vertical-align: 
                baseline	//default, The element is aligned with the baseline of the parent.
                sub	 //The element is aligned with the subscript baseline of the parent	
                super	//The element is aligned with the superscript baseline of the parent
                xpx|xcm	//Raises or lower an element by the specified length. Negative values are allowed. Read about length units	
                x%	//Raises or lower an element by a percent of the "line-height" property. Negative values are allowed
                
vertical-align: baseline|length|sub|super|top|text-top|middle|bottom|text-bottom|initial|inherit;
```
The ``text-align-last`` property specifies how to align the last line of a text

The ``direction`` property specifies the text direction/writing direction within a block-level element.

```
direction: ltr|rtl|initial|inherit;
           ltr	//default, Text direction goes from left-to-right	
           rtl	//Text direction goes from right-to-left	
           initial	
           inherit	
```

```
text-decoration: text-decoration-line text-decoration-color text-decoration-style text-decoration-thickness 

text-decoration-line: none|underline|overline|line-through|initial|inherit;

text-decoration-color: color|initial|inherit;

text-decoration-style: solid|double|dotted|dashed|wavy|initial|inherit;

text-decoration-thickness: auto|from-font|length/percentage|initial|inherit;
```
#### Test Indent

The ``text-indent`` property specifies the indentation/space of the first line in a text-block.

*Note: Negative values are allowed. The first line will be indented to the left if the value is negative*

```
text-indent : length|initial|inherit;
```
![image](https://user-images.githubusercontent.com/54256549/170817093-1e6e815e-6df0-437f-aed1-061ab798b1de.png)

#### Test Transform
```
line-height: 
             normal 
             number //A number that will be multiplied with the current font-size to set the line height
             length //A fixed line height in px, pt, cm, etc.
             x% //A line height in percent of the current font size
             initial
             inherit
letter-spacing: //letter-spacing property increases or decreases the space between characters
                normal
                length
                initial
                inherit

text-transform: none	//No capitalization. The text renders as it is. This is default	
                capitalize	//Transforms the first character of each word to uppercase	
                uppercase	//Transforms all characters to uppercase	
                lowercase	//Transforms all characters to lowercase	
                initial	//Sets this property to its default value. Read about initial	
                inherit	//Inherits this property from its parent element. Read about inherit

white-space: // helps control how whitespace and line breaks within an element's text are treated
              normal
              nowrap  //Text will never wrap to the next line. The text continues on the same line until a <br> tag is encountered
              pre //Text will only wrap on line breaks
              pre-line //text will wrap when necessary, and on line breaks
              pre-wrap  //Text will wrap when necessary, and on line breaks
              initial
              inherit
              
text-shadow: h-shadow v-shadow blur-radius color
             xpx ypx // horizontal shadow (xpx) and the vertical shadow (ypx)
             h-shadow v-shadow blur-radius
```

## Display

```
 display: 
```

#### Block
*An element that has the display property set to block starts on a new line and takes up the available screen width*

You can specify the width and heigh properties for such elements. 

Examples of elements that are at block-level by default are ``<div> <section> <p>``, and lots more

#### Inline
*An element with a display property set to inline will not start on a new line and it will take up the remaining/available screen width. It just takes up the space such an element would normally take*

you can't set the width and height of an element that has a display of inline, becuase it does not take up the whole screen width.

Some elements are inline by default, like ``<span>, <a>, <i>, and <img>``

#### Inline-block

*An element you assign a display of inline-block is inline by presentation. But it has the added advantage of you being able to apply width and height to it, which you can't do when the element is assigned a dispaly of inline.*

#### Flex

**Note :** *Its works on 2-axis i.e x-axis as ``main-axis`` and y-asix as ``cross-axis``*
**Note :** *Setting flex-direction as coloum it switch the main-axis to cross-axis and vica-versa. More formally ``justify-content and align-items`` are swtiched*

```
flex-direction: 
               row (default): left to right 
               row-reverse: right to left
               column: same as row but top to bottom
               column-reverse: same as row-reverse but bottom to top
```
```
flex-wrap: 
          nowrap (default): all flex items will be on one line. try to shink or overflow if more shinking is not possible
          wrap: flex items will wrap onto multiple lines, from top to bottom.
          wrap-reverse: flex items will wrap onto multiple lines from bottom to top. 
```

**Node :** *you can use ``flex-flow`` as a shorthand for the flex-direction and flex-wrap <br/>e.g:``flex-flow: column wrap``*

```
justify-content: // defines the alignment along the main axis
                  flex-start/start (default)
                  flex-end/end: items are packed toward the end of the flex-direction.
                  left: items are packed toward left edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like start.
                  right: items are packed toward right edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like start.
                  center: items are centered along the line through only main-axis
                  space-between: items are evenly distributed in the line; first item is on the start line, last item on the end line
                  space-around: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
                  space-evenly: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

```
```
align-items: //difines the alignment along with cross-axis(y-axis).Think of it as the justify-content version for the cross-axis
             stretch (default): stretch to fill the container (still respect min-width/max-width)
             flex-start / start / self-start: items are placed at the start of the cross axis. 
             flex-end / end / self-end: items are placed at the end of the cross axis. 
             center: items are centered in the cross-axis
             baseline: items are aligned such as their baselines align

```

**For both justify-content and align-items** *The safe and unsafe modifier keywords can be used in conjunction with all the rest of these keywords (although note browser support), and deal with helping you prevent aligning elements such that the content becomes inaccessible.*

```
align-content : // align-items works on signle whole row. if there are multiple row this help to adjust them
                normal (default)
                flex-start / start: items packed to the start of the container. The (more supported) flex-start honors the flex-direction while start honors the writing-mode direction.
                flex-end / end: items packed to the end of the container. The (more support) flex-end honors the flex-direction while end honors the writing-mode direction.
                center: items centered in the container
                space-between: items evenly distributed; the first line is at the start of the container while the last one is at the end
                space-around: items evenly distributed with equal space around each line
                space-evenly: items are evenly distributed with equal space around them
                stretch: lines stretch to take up the remaining space
```
![image](https://user-images.githubusercontent.com/54256549/170840215-42a2b1bc-d7f7-4270-8555-39f27227819b.png)
![image](https://user-images.githubusercontent.com/54256549/170840128-dc488804-c519-4bf3-a252-9e82c5632852.png)

```
gap: row-gap coloumn-gap

row-gap: xpx;
column-gap: xpx;
```

```
order: //the order property controls the order in which they appear in the flex container
       x px
```

```
flex : none or flex-grow flex-shrink flex-basis

flex-glow : // it indicate how much that flex item can increasse it size
            0  -> not increase at all, default
            greater than 1 // left over spaces are cal. and then divided into their %age e.g if flex glow=2 it will get twice the size of that free space
            
flex-shrink: //defines the ability for a flex item to shrink if necessary 
             1 default 
             0 no shinking allowed
             greater than 1
```
**Resource for flex tutorial is : yt(web made simplified** or https://css-tricks.com/snippets/css/a-guide-to-flexbox/

## Postion

```
position: static | relative | absolute | fixed | sticky | inheriet;
```
*Elements are then positioned using the top, bottom, left, and right properties but doesn't work on static*
```
static : default
         is not positioned in any special way
         it is always positioned according to the normal flow of the page
         static positioned elements are not affected by the top, bottom, left, and right properties.
```
