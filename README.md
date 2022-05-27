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


