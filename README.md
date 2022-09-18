# css-refresher 
> Cascading Style Sheets (CSS)
---
## CSS CSS Full Course for Beginner | Complete All-in-One by Dave Gray
> [(YOUTUBE) CSS Full Course for Beginner | Complete All-in-One by Dave Gray](https://www.youtube.com/watch?v=n4R2E7O-Ngo)
---
## Cascading Style Sheets (CSS) MDN
> [(MDN) Cascading Style Sheets (CSS)](https://developer.mozilla.org/en-US/docs/Web/CSS)
---
## Lesson 1 : Start Here
- HTML - like foundation and structure
- CSS  - like decorator
- External css by link in `<head></head>`
    - `<link rel="stylesheet" href="${placeOfFileCSS}">`
    - ```css
        p {
            color: purple;
            font-size: 64px;
        }
      ```
    - 
- Internal style tag in `<head></head>` in HTML
    - ```html
        <style>
            p {
                color: lightgreen;
            }
        </style>
      ```
- Inline CSS
    -  ```html
            <p style="color: blue;">I'm learning CSS!</p>
       ```
    - you need to avoid
    - This apply to the element 
- link first and style last
- display up to browser
- in chrome display last
> Common way use external stylesheet
## Anatomy of a CSS ruleset 
- [(MDN) Anatomy of a CSS ruleset](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics#anatomy_of_a_css_ruleset)

CSS Validator
[CSS Validator Service](https://jigsaw.w3.org/css-validator/validator)

---
## Lesson 2 : Selectors
- css selectors 3 levels
    - > 1. Element selector
    - select all of the element of that type
    -   ```css
            body {
                font-size: 22px;
            }

            p {
                color: purple;
            }
        ```
    - > 2. Class selector
    - start with period(".") and then the name of the class
    - apply all of project to reuse all element with class
    -   ```css
            .gray {
                color: gray
            }
        ```
    - > 3. Id selector
    - start with period("#") and then the name of the class
    - apply all of project to reuse all element with Id
    -   ```css
            #second {
                font-style: italic;
            }
        ```
    > group selector
    - `h1, h2 {...}`
    - Apply both h1 and h2 (by (","))
    -   ```css
            h1, h2 {
                color: blue;
            }
        ```
    > 
    - `h1 h2 {...}`
    - apply to h2 element inside h1 element (by (" "))
    -   ```css
            h1 h2 {
                color: blue;
            }
        ```
    - ex 
        -   ```css
                p span {
                    text-transform: uppercase;
                    background-color: gold;
                }
            ```
        - span insid paragraph
    > Universal selector 
    - select every thing on a page
    -   ```css
            * {
                font-family: monospace;
            }
        ```
    >seperate selector
        ```css
            li a {
                display: block;
            }
        ```
        - select anchor tag`<a></a>` inside list`<li></li>`
> css work
- CSS work like waterfloor  Top Down
- css apply by TOP DOWN
- class selector more spacific element selector
- css apply class selector before element selector
- css know rule of the specificity
    - last
    - class
- see by inspect right click inspect
- >spacific
    - >id > class > element
> inharitance
- some properties is inharitant
-   ```css
        button, input, textarea, select {
            font: inherit;
        }
    ```
> Don't USE `!important`
-   ```css
        p {
           color: purple!important;
        }
    ```
> Specificity Calculator
- [Specificity Calculator](https://specificity.keegan.st/)
- specify why working 
- more point is more specificity
---
## Lesson 3 : Colors
```css
    body {
        font-size: 22px;
        font-family: Arial, Helvetica, sans-serif;
        line-height: 1.5;
        background: #ffefd5;
        color: rgba(0, 0, 0,1);
    }

    p {
        color: #333333
    }
```
- `background-color: blue;`
- `background: papayawhip;` - short hand of `background-color: blue;`
- `color: darkblue;` - font color
    - name of color (color name)
        - `color: darkblue;`
    - rgb
        - `color: rgb(red, green, blue);` - can rgb
        - `color: rgb(0, 0, 0);`
    - rgba
        - `color: rgba(red, green, blue, alpha);` can rgba apha chanel
            - alpha 1 is normal
            - alpha 0 is disappear
            - alpha like opacity
        - `color: rgba(0, 0, 0,1);`
    - hexa decimal
        - `color: #000000`
        - #{red(f)}{red(f)}{green(f)}{green(f)}{blue(f)}{blue(f)}
    - mouse click and select color
> Color pallettes generator
- [Coolers.co](https://coolors.co/)
- [WebAim](https://webaim.org/)
---
## Lesson 4 : Units & Sizes
- [(MDN) Absolute length units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#numbers_lengths_and_percentages)
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    width: 100%;
    min-height: 100vh;
}

h1 {
    border: 2px dashed red;
    width: 50%;
    font-size: 3rem;
    padding: 0.5em;
}

main {
    font-size: 2rem;
}

p {
    font-size: 2rem;
    width: 40ch;
}
```
- font-size default 16px
- absolute value
    - pixel
- relative value
    - relative to the parent
    - percent(%)
    - rem (root emphasize) - Font size of the root element. 
        - root element defind by browser.
    - em (emphasize) - Font size of the parent, in the case of typographical properties like font-size, and font size of the element itself, in the case of other properties like width.
    - ch (charector) - The advance measure (width) of the glyph "0" of the element's font. (charector before the line wrap)
    - vw (viewport's width) - 1% of the viewport's width. `(like use percent(%))` `use percent(%) instant`
    - vh (viewport's height) - 1% of the viewport's height.

- font-size - use `rem`
- padding or margin - use `em`
- `em` relate font-size
---
## Lesson 5 : Box Model
- inspect 
    - orange - margin 
    - green - padding
    - blue -content
- box-sizing
    - content-box
    - border-box
- margin
    - Long hand
        ```css
        .container {
            margin-top: 1.5em;
            margin-right: 2em;
            margin-bottom: 2em;
            margin-left: 2em;
        }
        ```
    - Short hand
        ```css
        .container {
            margin: top rightandleft bottom ;
            margin: topandbottom rightandleft ;
            margin: top right bottom left ;
        }
        ```
    - left and right
        ```css
        .container {
            margin: 3rem auto;
        }
        ```
- padding
    - Long hand
        ```css
        .container {
            padding-top: 1.5em;
            padding-right: 2em;
            padding-bottom: 2em;
            padding-left: 2em;
        }
        ```
    - Short hand
        ```css
        .container {
            padding: top rightandleft bottom ;
            padding: topandbottom rightandleft ;
            padding: top right bottom left ;
        }
        ```
- border 
    - border
        ```css
        .container {
            border: 2px dashed red;
        }
        ```
    - Long hand
        ```css
        .container {
            border-top-width: 5px;
            border-top-style: dotted;
            border-top-color: blue;
        }
        ```
    - Short hand
        ```css
        .container {
            border-top: 5px solid green;
        }
        ```
- outline
    - outline
        ```css
        .container {
             outline: 5px solid purple;
            outline-offset: 5px;
        }
        ```
- circle
    ```css
        .container {
            margin: 3rem auto;
            background-color: gold;
            width: 100px;
            height: 100px;
            border: 2px solid black;
            border-radius: 50px;
            outline: 2px solid red;
            outline-offset: 0.25rem;
        }
    ```
---
## Lesson 6 : Typography
- Typography is the way that text is arranged and presented.
> [(MDN) text-menu](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
- Text-decoration
    ```css
        p {
            text-decoration: underline;
            text-decoration: overline;
            text-decoration: line-through;
            text-decoration: none;
        }   
    ```
    - default is none
- Text-transform
    ```css
        p {
            text-transform: capitalize;
            text-transform: lowercase;
            text-transform: uppercase;
        }   
    ```
- Text-align
    ```css
        p {
            text-align: left;
            text-align: justify;
            text-align: right;
        }   
    ```
    - default is left
- Text-indent
    ```css
        p {
            text-indent: 2em;
        }   
    ```
    - indent in first line.
- Line-height
    ```css
        p {
            line-height: 1.5;
        }   
    ```
- Letter-spacing
    ```css
        p {
            letter-spacing: 0.25em;
        }   
    ```
- Word-spacing
    ```css
        p {
            word-spacing: 0.5em;
        }   
    ```
- Font-weight
    ```css
        p {
            font-weight: 100;
            font-weight: bolder;
        }   
    ```
    - default is 300 - 400
- Font-style
    ```css
        p {
            font-style: italic;
            font-style: oblique;
        }   
    ```
    - default is normal
- Font-family
    ```css
        p {
            font-family: sans-serif;
            font-family: monospace;
            font-family: cursive;
            font-family: fantasy;
            font-family: first choice, second choice, third choice;
            font-family: 'Courier New', Courier, monospace;
            font-family: Arial, Helvetica, sans-serif;
            font-family: Verdana, Geneva, Tahoma, sans-serif;
            font-family: 'Times New Roman', Times, serif;
        }   
    ```
>[Google fonts](https://fonts.google.com/)
- link
    - In HTML file
    ```html 
        <head>
        ...
            <link rel="preconnect" href="https://fonts.googleapis.com">
            <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
            <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300&family=Roboto:ital@1&display=swap" rel="stylesheet">
        </head>
    ```
    ```css
        body {
            font-family: 'Roboto', sans-serif;
        }
    ```
    - In CSS file only
    ```css
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300&family=Roboto:ital@1&display=swap');

        body {
            font-family: 'Roboto', sans-serif;
        }
    ```
---
## Lesson 7 : Styling Links
- link (a tag (archor tag))
- Text decouration 
    ```css
       a {
            text-decoration: underline;
            text-decoration: none;
        }
    ```
- Cursor
    ```css
       a {
            cursor: not-allowed;
            cursor: pointer;
        }
    ```
- Color
    ```css
       a {
                color: blue;
        }
    ```
    - default is blue
- Psudo class
    - visited
        ```css
        a:visited {
            color: black;
        }
        ```
    - hover
        ```css
        a:hover {
            color: dodgerblue;
        }
        ```
    - active
        ```css
        a:active {
            color: red;
        }
        ```
    - focus 
        ```css
        a:focus {
            color: lightsalmon;
        }
        ```
    - same style hover and focus
        ```css
        a:hover,a:focus  {
            color: dodgerblue;
        }
        ```
- Opacity
    - opacity
        ```css
        a:hover,a:focus  {
            opacity: 0.8;
        }
        ```
    - opacity max is 1 
    - opacity min is 0 is transparent
- background
    ```css
        a:hover,a:focus  {
            background-color: gold;
        }
    ```
---
## Lesson 8 : List Styles
- List style type
    ```css
        ol {    
            list-style-type: lower-alpha ;
            list-style-type: georgian;
            list-style-type: decimal;
            list-style-type: decimal-leading-zero;
            list-style-type: disc;
            list-style-type: circle;
            list-style-type: upper-roman;
            list-style-type: none;
            list-style-type: square;
        }
    ```
    - default is decimal.
    - custom start
        ```html
        <ol start="3">
            <li>Step One</li>
            <li>Step Two</li>
            <li>Step Three</li>
        </ol>
        ```
    - count down 
        ```html
        <ol reversed>
            <li>Step One</li>
            <li>Step Two</li>
            <li>Step Three</li>
        </ol>
        ```
- Text align
    ```css
        ul {
            text-align: center;
        }
    ```
- List style position
    ```css
        ul {
            list-style-position: inside;
        }
    ```
    - default chrome is outside
- List style images
    ```css
        ul {
            list-style-image: url('../images/checkmark.png');
        }
    ```
- List style shorthand
    ```css
        ul {
            list-style: square url('../images/checkmark.png') inside;
        }
    ```
    - `list-style: list-style-type list-style-image list-style-position;`
- change list
    - change all list
        ```css
            ul li:nth-child(even) {
                color: red;
            }
        ```
    - change list in unorder list
        ```css
            ul li:nth-child(even) {
                color: red;
            }
        ```
    - change list in unorder list in child `2`
        ```css
            ul li:nth-child(2) {
                color: red;
            }
        ```
    - change list in unorder list in child `odd`
        ```css
            ul li:nth-child(odd) {
                color: red;
            }
        ```
    - change list in unorder list in child `even`
        ```css
            ul li:nth-child(even) {
                color: red;
            }
        ```
- psudo class marker
    - `::marker`
    - change all marker
        ```css
            ::marker {
                color: red;
                font-family: fantasy;
                font-size: 1em;
                content: "only $5 >>";
            }
        ```
    - change marker in unorder list
        ```css
            ul ::marker {
                color: red;
                font-family: fantasy;
                font-size: 1em;
                content: "only $5 >>";
            }
        ```
- content 
    - change content of bullet
        ```css
            ul ::marker {
                content: "only $5 >>";
            }
        ```
- change value of list
    - In HTML File
        ```html 
            <li value="26">Step Two</li>
        ```
---
## Lesson 9 : Mini Project
- border-radius 
    ```css
        h2 {
            padding: 1rem;
            background: gold;
            border-radius: 2rem 2rem 0 0;
        }
    ```
    - border-radius: topleft topright bottomright bottomleft;
- border-top
    ```css
        li {
            border-top: 1px solid #333;
        }
    ```
- other
    ```css
        li a,
        li a:visited {
            text-decoration: none;
            color: #333;
        }
    ```
    ```css
        li a:hover, 
        li a:focus {
            background: #333;
            color: whitesmoke;
            cursor: pointer;
        }
    ```
- display
    ```css
        li a {
            display: block;
        }
    ```
    - a tag is inline display
    - block display is 100% width
        - inline display 
        - block display
- psudo select 
    - last-child
        ```css
            li:last-child a {
                border-radius: 0 0 2rem 2rem;
            }
        ```
---
## Lesson 10 : Display
- block
    - html is block element
    - 100% width
    - block can stack of top each other.
- inline
    - `span` is default display `inline`
    - inline do not stack of top each other.
    - only width of the content
- inline-block
    - hyblid
    - inline and can top and bottom, hight  
    ```css
        .opposite {
            display: inline-block;
            background-color: #333;
            color: whitesmoke;
            padding: 4rem;
            margin-top: 100px;
            height: 200px;
        }
    ```
    ```css
        li {
            display: inline-block;
            margin-inline: 0.5rem;
        }
    ```
- use every element 
    ```css
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
    ```
---
## Lesson 11 : Float
index.html
```html
    <body>
        <section>
            <div class="block left">Float</div>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Amet natus repudiandae itaque? Aliquam accusamus autem corporis ad sint, eum, eveniet, omnis velit ipsum temporibus ex quisquam iure aspernatur debitis quam!</p>
        </section>
        <div class="clear"></div>
        <p>Nam, autem doloremque, rerum perspiciatis cumque voluptatem, nisi ex quibusdam atque quos itaque sed quasi vitae dignissimos. Perspiciatis aspernatur, dolorum natus mollitia voluptatibus vitae adipisci quia porro id vel voluptate.</p>
        <p>Optio accusamus perferendis blanditiis laborum perspiciatis provident similique commodi nostrum totam cumque sunt error earum, doloribus architecto illum voluptatem ea! Ipsam aut impedit provident sed delectus quis dignissimos est dolores!</p>
        <div class="block right">Float</div>
        <p>Ab, laborum mollitia incidunt sit dolore maxime at repudiandae ut dolorum dicta cum? Tempora aperiam numquam ut adipisci ducimus totam placeat quod, amet odio possimus ex repellendus, rem vitae animi!</p>
        <p>Obcaecati quia nisi ut hic delectus sit odit, eum tempore ipsum unde neque eos incidunt numquam facilis distinctio rerum quasi. Optio illo incidunt aspernatur dolores unde reiciendis quis, beatae sit.</p>
        </section>
    </body>
```
/css/style.css
```css
    @import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

    body {
    font-size: 1.5rem;
    font-family: "Roboto", sans-serif;
    }

    .block {
        width: 30vw;
        height: 30vw;
        background-color: #000;
        color: #fff;
        padding: 1rem;

    }

    .left {
        float: left;
        margin-right: 1rem;
    }

    .right {
        float: right;
        margin-left: 1rem;
    }

    .clear {
        clear: both;
    }

    section {
        background-color: bisque;
        border: 1px solid #333;
        padding: 1rem;
        display: flow-root;
    }
```
- Float
    - float 
        - left
        - right
- Clear
    - clear
        - left
        - right
        - both
    - clear paragraph
- Overflow
    - section contain all float
    ```css
        section {
            background-color: bisque;
            border: 1px solid #333;
            padding: 1rem;
            overflow: auto;
        }
    ```
- display : flow-root
    - section contain all float
    ```css
        section {
            background-color: bisque;
            border: 1px solid #333;
            padding: 1rem;
            display: flow-root;
        }
    ```
    ---
## Lesson 11 : Columns
