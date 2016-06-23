#React

[React JS Tutorial for Beginners - 3 - Multiple Components and Properties](http://bit.ly/1VBqhUe)

User Interface Library ( created by Facebook )
Has Virtual DOM which makes it fast to load pages, insert new content into DOM efficiently
Uses JSX syntax ( inside script tag <script type= text/jsx></script> )


<script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.13.3/react.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.13.3/JSXTransformer.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>

____________

Component :
    building block for UI
    is a react class.
```javascript
    var componentName = React.createClass({
        // code
    })
```
Each component has a render function which returns html content which will be rendered to the page.

```javascript
    var componentName = React.createClass({
        render: function () {
            return (
                <h2>Hey there!</h2>
            );
        }
    })
```
_________

Render, takes two arguments, component to display & where to display it ( div etc. )

```javascript
React.render(
     <componentName />,
    document.getElementById('content')
);
```
_____________

slush pages-react ( scaffolding tool/generator )

uses ES6 :
e.g.
    import React from 'react'
    import { render } from 'react-dom'

JSX:
    new language( looks a bit like html in your js file ) mix of js & html
    doesn't like comments
    JSX is a preprocessor step that adds XML syntax to JavaScript

Uses a dev-server ( localhost )

jquery & react don't really belong together

____________________

Every react class needs to have a render function which returns code which resembles html
components are reusable
class name needs to start with capital letter..

Props is an immutable value ( never changes ). Props is an object
you can set props when you create a new instance of a component

State ( & setState )
    changes over time, based on user interaction etc.
