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
