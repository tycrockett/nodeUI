# Print Example

```
const { print } = require('simple-node-ui');

const value = 'World';

print(`
  <style:bgCyan,black width:.5 align:right rightSpace:1>
  "Hello"
  <align:left>
  "${value}"

  <nl:2 style:reset emptyChar:- width:max align:center>
  "TEST"

  <nl>
`);
```

## Print Values
```
width            

          min (default)
          Sets the width to the length of the string

          max
          Sets the width to terminal width

          n
          Sets the width to n characters

          n (0-1)
          Any number between 0 and 1 is a percent of the terminal width

align            

          left (default)
          Sets alignment to the left

          right
          Sets alignment to the right

          center
          Sets alignment to the center

emptyChar          

          When the width is greater than the strings length the remaining
          width is filled with emptyChar.

leftSpace / rightSpace   

          n
          Adds space to the left/right side by n characters

          n (0-1)
          Adds space to the left/right side by n percent of the window

style            

          Multiple styles should be separated by commas, ie style:reset,black,bgWhite

          FORMATS
               reset
               bright
               dim
               underscore
               blink
               reverse
               hidden

          COLORS
               red
               green
               black
               yellow
               blue
               magenta
               cyan
               white

          BACKGROUND COLORS
               bgBlack
               bgRed
               bgGreen
               bgYellow
               bgBlue
               bgMagenta
               bgCyan
               bgWhite



```

## styles
```
const { styles } = require('simple-node-ui);
const { underscore } = styles;
console.log(`${underscore}Hello`);
```

## getScreenWidth, getScreenHeight
```
const { print, getScreenWidth, getScreenHeight } = require('simple-node-ui');
const width = getScreenWidth();
print(`
     <width:${width - 4} align:right>
     "Width subtract four characters"
`);
```

## buildEmptySpace
```
const { print, buildEmptySpace } = require('simple-node-ui');
const stars = buildEmptySpace(5, '*');
print(`
     "${stars} 5 Stars"
`);
```