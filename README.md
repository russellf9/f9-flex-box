# f9-flex-box
A repository for my study of Flex Box

## CSS Positioning

Vertical and horizontal alignment is a corner stone of CSS UI. Rather than at this stage, going back to the old ways I thought I should focus on the current best technology.

Of course **Flex Box** isn't fully backward compatible, but if my focus is mobile development then this is definitely the course to take.

And, **Flex Box** seems more like the "semantic-web" rather than using tables or negative margins, not forgetting it's very much like Flex!

There are some Safari webkit [compatibility issues](http://caniuse.com/#feat=flexbox) which are easily fixed by using the <code>-webkit</code> prefix. Which in turn will lead me to using [SASS](http://sass-lang.com) or another pre-compiler.

(This I would do with Gulp [gulp-ruby-sass](https://github.com/sindresorhus/gulp-ruby-sass) - see: [A Beginners Guide to the Task Runner Gulp](http://andy-carter.com/blog/a-beginners-guide-to-the-task-runner-gulp) )

I've generally run through the tutorial on [THE ULTIMATE FLEXBOX CHEAT SHEET](http://www.sketchingwithcss.com/samplechapter/cheatsheet.html).


### Examples

(I`ve kept the Webkit prefix for Safari in these examples.)

## Center both horizontal and vertical

```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-align-items: center;
    align-items: center;
}
```

## Space between

<cite>"..items are evenly distributed in the line; first item is on the start line, last item on the end line...<cite>

( See: [justify-content](http://css-tricks.com/almanac/properties/j/justify-content/) )

```
.flex-container-space-between {
    display: -webkit-flex;
    display: flex;
    -webkit-justify-content: space-between;
    justify-content: space-between;
    -webkit-align-items: center;
    align-items: center;
}
```

### Space around

<cite>"..items are evenly distributed in the line with equal space around them...<cite>

```
.flex-container-space-around {
    display: -webkit-flex;
    display: flex;
    -webkit-justify-content: space-around;
    justify-content: space-around;
    -webkit-align-items: center;
    align-items: center;
}
```

### Row


```
.flex-container-row {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: row;
    flex-direction: row;
}

```


### Column


```
.flex-container-column {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: column;
    flex-direction: column;
}

```

## All directions ( ie all items will be aligned vertically and horizontally. )

```
.flex-container-all {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: row /* works with row or column */
    flex-direction : row;
    -webkit-align-items: center;
    align-items: center;
    -webkit-justify-content: center;
    justify-content: center;
}
```

### Define end or start points

(Looks like that `flex-start` is the default.)

```
# if used in column the first item will align to the top
# if used in row the first item will align to the left
    -webkit-justify-content: flex-start;
    justify-content: flex-start;

```

```
# if used in column the first item will align to the bottom
# if used in row the first item will align to the right
    -webkit-justify-content: flex-end;
    justify-content: flex-end;
```


### Reverse (TODO)

```
/* Reverse row */
.flex-container-row-reverse {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: row-reverse;
    flex-direction: row-reverse;
    -webkit-align-items: center;
    align-items: center;
}
```


## Links

* [THE ULTIMATE FLEXBOX CHEAT SHEET](http://www.sketchingwithcss.com/samplechapter/cheatsheet.html)
* [centering-css-complete-guide](http://css-tricks.com/centering-css-complete-guide/)
* [Goodbye floats and clearfixes.](http://www.sketchingwithcss.com/flexbox-tutorial/)
* [flex-direction](http://css-tricks.com/almanac/properties/f/flex-direction/)
