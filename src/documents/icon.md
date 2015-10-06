---
title: Navigation Icon
layout: default
category: API
---

## Overview

**Component Name:** `gpii.firstDiscovery.icon`

**File:** `navIcons.js`

A component wrapper around a single navigational icon, managing the state (active/inactive, confirmed).

## Adding a Navigation Icon component

*Option 1*: Typically this component is used as a sub-component of the [Navigation Icons](navIcons.md):
```javascript
icon: {
    type: "gpii.firstDiscovery.icon",
    container: "{that}.dom.icon",
    options: {...}
}```

*Option 2*: Outside the context of the First Discovery Tool, developers may wish to create a standalone component:
```javascript
var myNavIcon = gpii.firstDiscovery.icon(container, options);
```


## Grades

The base [grades](http://docs.fluidproject.org/infusion/development/ComponentGrades.html)
used by the the First Discovery Editor:

* [`fluid.viewComponent`](http://docs.fluidproject.org/infusion/development/ComponentGrades.html)

## Model

| Path   | Description | Values | Default |
|--------|-------------|--------|---------|
| `isActive` | Whether the icon is active (i.e. the related panel is visible) | Boolean | undefined  |
| `isConfirmed` | Whether the icon is confirmed (i.e. the related panel adjuster has been confirmed) | Boolean | undefined  |

## Options

<table>
    <tr><th>Name</th><th>Description</th><th>Values</th><th>Default</th></tr>
    <tr>
        <td>`position`</td>
        <td>The index of the icon, within the set of all navigation icons.</td>
        <td>Number</td>
        <td>
        <pre><code>position: null</code></pre>
        </td>
    </tr>
    <tr>
        <td>`selectors`</td>
        <td>Javascript object containing selectors for various fragments of the markup, including the containers for the subcomponents.</td>
        <td></td>
        <td>See [Selectors](#selectors) below</td>
    </tr>
    <tr>
        <td>`styles`</td>
        <td>Specific class names used to achieve the look and feel</td>
        <td></td>
        <td>
        <pre><code>styles: {
    active: "gpii-fd-active",
    show: "gpii-fd-show"
}</code></pre>
        </td>
    </tr>
    <tr>
        <td>`modelListeners`</td>
        <td>JavaScript object containing model paths and the listeners that are activated when changes happen to those paths</td>
        <td>Keys in the object are event names, values are functions or arrays of functions.</td>
        <td>See [Model](#model) above</td>
    </tr>
</table>

## Selectors

One of the options that can be provided to the First Discovery Editor is a set of CSS-based
selectors identifying where in the DOM different elements can be found. The value for the option
is itself a Javascript object containing name/value pairs:

```javascript
selectors: {
    selector1Name: "selector 1 string",
    selector2Name: "selector 2 string",
      ...
}
```

| Selector Name | Description | Default |
|---------------|-------------|---------|
| `confirmedIndicator` | The confirmation badge that will be applied to the icon after its related panel's adjuster has been confirmed | `".gpiic-fd-confirmedIndicator"` |

## Dependencies

```html
<script type="text/javascript" src="src/lib/infusion/infusion-custom.js"></script>
<script type="text/javascript" src="src/js/navIcons.js"></script>
```
