---
title: Sticky Keys Adjuster
layout: default
category: API
---

## Overview

**Component Name:** `gpii.firstDiscovery.keyboard.stickyKeysAdjuster`

**File:** `stickyKeysAdjuster.js`

Creates the interface for users to experiment the keyboard feature when the sticky keys
preference is turned on or off.

## Using the Sticky Keys Adjuster

*Option 1*: Typically this component is used as a sub-component of the [Sticky Keys](keyboard.md) panel:
```javascript
assistance: {
    type: "gpii.firstDiscovery.keyboard.stickyKeysAdjuster",
    container: "{that}.container",
    options: {}
}
```

*Option 2*: Outside the context of the First Discovery Tool, developers may wish to create a standalone component:
```javascript
var myStickyKeysAdjuster = gpii.firstDiscovery.keyboard.stickyKeysAdjuster(container, options);
```


## Grades

This component uses the following base
[grades](http://docs.fluidproject.org/infusion/development/ComponentGrades.html):

* [`gpii.firstDiscovery.attachTooltip`](attachTooltip.md)
* [`gpii.firstDiscovery.msgLookup`](msgLookup.md)
* [`fluid.viewComponent`](http://docs.fluidproject.org/infusion/development/ComponentGrades.html)

## Model

This component supports the following
[model](http://docs.fluidproject.org/infusion/development/tutorial-gettingStartedWithInfusion/ModelComponents.html)
properties:

| Path   | Description | Values | Default |
|--------|-------------|--------|---------|
| `stickyKeysEnabled` | Whether or not the sticky keys preference is turned on. | Boolean | undefined |
| `tryAccommodation ` |Whether or not the user has chosen to try the sticky keys feature.  | Boolean | undefined |

## Methods

| Method | Description | Parameters |
|--------|-------------|------------|
| `toggleStickyKeys` | Toggles `model.stickyKeysEnabled` between an enabled/disabled state. | none  |
| `toggleTry` | Toggles `model.tryAccommodation` between an enabled/disabled state. | none  |

## Options

This component can be configured using the following
[options](http://docs.fluidproject.org/infusion/development/ComponentOptionsAndDefaults.html):

<table>
    <tr><th>Name</th><th>Description</th><th>Values</th><th>Default</th></tr>
    <tr>
        <td>`selectors`</td>
        <td>Javascript object containing selectors for various fragments of the markup, including the containers for the subcomponents.</td>
        <td></td>
        <td>See [Selectors](#selectors) below</td>
    </tr>
</table>

## Selectors

{{>selectorsIntro}}

| Selector Name | Description | Default |
|---------------|-------------|---------|
| `description` | The description of why the sticky keys feature is useful. | `".gpiic-fd-keyboard-stickyKeysAdjuster-desc"` |
| `tryButton` | The try it button. | `".gpiic-fd-keyboard-stickyKeysAdjuster-try"` |
| `accommodation` | The wrapper container of elements to operate the sticky keys feature. Typically includes these elements: `accommodationInstr`, `accommodationName`, `accommodationState`, `accommodationToggle` | `".gpiic-fd-keyboard-stickyKeysAdjuster-accommodation"` |
| `accommodationInstr` | The description of an example of how to use the sticky keys feature. | `".gpiic-fd-keyboard-stickyKeysAdjuster-accommodationInstr"` |
| `accommodationName` | The label of "Sticky Keys". | `".gpiic-fd-keyboard-stickyKeysAdjuster-accommodationName"` |
| `accommodationState` | The current on/off state of the sticky keys feature. | `".gpiic-fd-keyboard-stickyKeysAdjuster-accommodationState"` |
| `accommodationToggle` | The button to toggle the on/off state of the sticky keys feature. | `".gpiic-fd-keyboard-stickyKeysAdjuster-accommodationToggle"` |

## Dependencies

```html
<script type="text/javascript" src="src/lib/infusion/infusion-custom.js"></script>
<script type="text/javascript" src="src/js/tooltip.js"></script>
<script type="text/javascript" src="src/js/msgLookup.js"></script>
<script type="text/javascript" src="src/js/navButtons.js"></script>
```

