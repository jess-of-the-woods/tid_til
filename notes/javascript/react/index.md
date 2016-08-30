[JavaScript](../index.md) | [frontend](../../frontend.md) | [client-side](../../client-side.md)

## React.js
<a href='https://facebook.github.io/react/'><img src="http://yycjs.com/real-world-react/img/react-logo.png" width="150"></a>

**[Redux](redux.md)** | **Router**

User Interface Library created by Facebook

Has Virtual DOM which makes it fast to load pages, insert new content into DOM efficiently

Uses JSX syntax (inside script tag `<script type='text/jsx'></script>`)

- [jQuery](../javascript/jquery.md) & react don't really belong together.
- Uses a dev-server ( localhost )
- Every react class needs to have a render function which returns code which resembles HTML
- components are reusable
- class name needs to start with capital letter..

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.13.3/react.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.13.3/JSXTransformer.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
```

### Component
- building block for UI
- is a react class.


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

### Render function
(from module) takes two arguments, component to display & where to display it (e.g. a div). This is typically the top-level component, inside which others are rendered (nested?)

```javascript
React.render(
     <componentName />,
    document.getElementById('content')
);
```

#### Props
- is an immutable value ( never changes ). Props (properties) is an object.
You can set props when you create a new instance of a component.

#### State ( & setState )
- changes over time, based on user interaction etc. You can call setState on state to mutate it.

#### JSX
- new language( looks a bit like [HTML](../HTML.HTML.md) in your js file ) mix of js & HTML
- doesn't like comments
- JSX is a preprocessor step that adds XML syntax to JavaScript

---

**slush-pages-react** npm module (slush scaffolding tool/generator)

([documentation](https://www.npmjs.com/package/slush-pages-react))

type `slush pages-react` inside a folder

Uses ES6 e.g.

```javascript
import React from 'react'
import { render } from 'react-dom'
```

---

### Links
- [React JS Tutorial for Beginners - 3 - Multiple Components and Properties](https://www.youtube.com/watch?v=JR-Cr_PSVV4&list=PL6gx4Cwl9DGBhLZx_5C-jqECBE4HIID_k&index=3) - YouTube series

See also Angular, Ember..
