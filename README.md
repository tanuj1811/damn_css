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

```
background-repeat: repeat /**default, repeat over both axis x as well as y*/
                   no-repeat 
                   repeat-x /* repeat over x- axis**/
                   repeat-y
```

```
background-position: center; /* Center the image */
```

