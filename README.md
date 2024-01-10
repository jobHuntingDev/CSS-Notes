# CSS notes

## Fonts

Changing font styles

```css
h1{
	font-family: "press Start 2P";
}
p{
	font-family: "consolas", sans-serif;
	font-syle: italic;
	font-weight: bold;
	text-decoration: blue dotted underline;
	font-size: 18px;
}
```

## Borders

```css
h1{
	border-top-style: dotted;
	border-bottom-style: dotted;
	border-left-style: double;
	border-left-width: 10px;
	border-left-color: silver;
}

p{
	border-style: solid;
	border-width: 5px;
	border-color: green;
	border-radius: 100px;
}
```

## Backgrounds

```css
body{
	background-color: blue;
}

header{
	background-image: url("./myBackground.jpg");
	background-repeat: no-repeat;
	background-attachment: fixed;
	background-position: center;
	background-size: cover;
}

main{
	background: linear-gradient(skyblue, lightgreen);
	background-repeat: no-repeat;
	background-attachment: fixed;
}

footer{
	background: linear-gradient(to right, skyblue, lightgreen);
}
```
## Position

static: default
relative: Move object relative to some point of origin.usually top-left
absolute: Taken out of flow of documents. It's like it's a ghost. Will search for parent (positioned anything other than static and will be positioned relative to said parent.
fixed: will stay where you set it.
sticky: Stick to the top or bottom


```css
#box1{
	border: 1px solid;
	height: 300px;
	width: 300px;
	background-color: skyblue;

	
	position:relative;
	top: 50px;
	left: 50px;
}

#box2{
	border: 1px solid;
	height: 100px;
	width: 100px;
	background-color: red;

	position: absolute:	
	top:0;
}

#box3{
	border: 1px solid;
	height: 100px;
	width: 100px;
	background-color: orange;

	position: fixed;
	top:0px;
	right: 0px;
}

#box4{
	border: 1px solid;
	height: 100px;
	width: 100px;
	background-color: orange;

	position: stickey;
	top:0px;
	bottom: 0px;
}
```

## Pseudo classes

pseudo-class = a keyword added to a selector that specifies a special state of the selected element(s)

```css
a:link{
	color: lawngreen;
}

a:visited{
	color: grey;
}

a:hover{
	color: yellow;
}

a:active{
	color: orange;
}

button:hover{
	background-color: lightgrey;
}

button:active{
	background-color: white;
}

/*
li:nth-child(2){
	background-color: yellow;
}

li:nth-child(even){
	background-color: yellow;
}

li:nth-child(odd){
	background-color: yellow;
}
*/

li:nth-child(5n+2){
	background-color: yellow;
}
```

## Shadows

```css
/* Text shadows */
text-shadow: x y spread colour;
h1{
	text-shadow: 0px 0px 5px yellow;
}

/* Box shadows */
box-shadow: x y spread colour;
h1:hover{
	box-shadow: 5px 5px 5px black;
}
```

## Transform

```css
#box1{
	border: 4px solid;
	width: 250px;
	height: 225px;
	font-size: 225px;
	text-align: center;
	background: lightskyblue;

	/*
	transform: translateX(50px);
	transform: translateY(50px);
	*/	
	
	/* transform: translate(x,y); */
	transform: translate(50px, 50px);

	transform: rotateX(50px);
	transform: rotateY(50px);
	transform: rotateZ(50px);
	
	/*
	transform: scaleX(3);
	transform: scaleY(3);
	*/	
	
	/* transform: scale(x,y); */
	transform: scale(50px, 50px);

	
	/*
	transform: skewX(45deg);
	transform: skewY(45deg);
	*/	
	
	/* transform: skew(x,y); */
	transform: skew(20deg, 20deg);	
}
```

## Animateion with CSS Transitions

```css
body {

}

.box {
	width: 300px;
	height: 300px;
	background: #3DCCC7;
	transition-duration: 100ms;
	transition-property: background, transform;
}

.box:hover{
	background: #FFBBBB;
	transform: rotate(45deg);
}
```

Transition Timing Function:

Options can be found in 

```css
.box {
	width: 200px
	height: 200px;
	transition-duration: 2000ms;
	transition-propert: background, transform;
	transition-timingfunction: ease-in;
}
```

Transition delay:

```css
.box {
	width: 200px
	height: 200px;

	transition-duration: 2000ms;
	transition-propert: background, transform;
	transition-timingfunction: ease-in;
	transition-delay: 200ms;
}
```

## CSS custom properites

```css
:root{
	--bg: #9034390;
	--title-tx: #865349;
}

p{
	background-color: var(--bg);
}
```
## Flex Box

```css

.container{
	display: flex;

	flex-direction: column;
	\* Options:
		row
		row-reverse
		column
		column-reverse
	*/
	
	justify-content: center;
	/* Options
		flex-start	
		flex-end
		center
		space-between
		space-around
		space-evenly
	*/

	align-items: flex-start;
	/* Options
		flex-start
		flex-end
		center
		baseline: aline text
	*/

	flex-wrap: wrap;
	/* Options
		nowrap
		wrap
		wrap-reverse
	*/

	aling-content: flex-start;
	/* Options
		flex-start
		flex-end
		center
		space-evenly
		space-between
	*/

	column-gap: 10px;
	row-gap: 20px
}

.box{
	width: 150px;
	height: 150px;
	font-size: 8em;
	text-align: center;
	border-radius: 15px;
}

#box1{
	background-color: red;
}

#box2{
	background-color: yellow;
	order: 1;
}

#box3{
	background-color: green;
	order: -1;
}

#box4{
	background-color: lightblue;
}
```

## Grid

```css
.testimonial-grid {
	display: grid;
	gap: 1.5rem;
	grid-template-columns: repeat(4, 1fr);
}

.grid-col-span-2 {
	grid-column: span 2;
}

/* Using line numbers */
.testimonial:last-child {
	grid-column-start: 4;
	grid-row-start: 1;
	grid-row: span2;
}
```
