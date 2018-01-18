
## init
### When
Runs once on instatiation of this component
### Use

### Example

### Syntax

```javascript
init() {
    this._super(...arguments);
},
```

## didReceiveAttrs
### When
Runs after init and on subsequent re-renders (unless this has triggered internally) if the components attributes have changed.
### Use
Can be thought of as an observer, runs logic every time an attribute changes.
### Example
If you have some data in an attr that may change type but should be internally consistent within the component, checks and conversion can happen here.
### Syntax
```javascript
didReceiveAttrs() {
    this._super(...arguments);
},
```

## didRender
### When
Called during both render and re-render after template has and DOM has updated.
### Use
Usually used to perform post processing on the DOM after it's been updated.
### Example
After causing a re-render on a long list, finding the currently selected option and scrolling to that position.
### Syntax
```javascript
didRender() {
    this._super(...arguments);
},
```

## didUpdate
### When
Called once the component has finished updating itself
### Use
(Re)enable fields that relied on a component updating.
### Example
A submit button is desabled on action, enabled once the return from submission updates a field on the form.
### Syntax
```javascript
didUpdate() {
    this._super(...arguments);
},
```

## didUpdateAttrs
### When
Prior to a re-render that is triggered by an attr change (not a forced re-render via `component.rerender`).
### Use
To execute code when a specific attr changes, can be an effective alternative to an observer.
### Example
Useful for fixing validation UI notifications, IE an invalid input warning that then becomes valid.
### Syntax
```javascript
didUpdateAttrs() {
    this._super(...arguments);
},
```

## didInsertElement
### When
Once the component's element has been inserted into the DOM AND is accessible via the components $() method.
### Use
Initialising anything that requires a DOM node to bind to.
### Example
Adding a third party date picker to a form.
### Syntax
```javascript
didInsertElement() {
    this._super(...arguments);
},
```

## didDestroyElement
### When
After component is destroyed
### Use

### Example

### Syntax
```javascript
didDestroyElement() {
    this._super(...arguments);
},
```

## willRender
### When
On both render and re-render this is called when
### Use

### Example

### Syntax
```javascript
willRender() {
    this._super(...arguments);
},
```

## willUpdate
### When
On re-render this is called before the component updates
### Use

### Example

### Syntax
```javascript
willUpdate() {
    this._super(...arguments);
},
```

## willDestroyElement
### When
When a component detects that it should remove itself from the DOM
### Use
Run teardown logic for that component.
### Example
Removing listeners for elements within a component before it is destroyed. Updating UI based on elements existing/being destroyed.
### Syntax
```javascript
willDestroyElement() {
    this._super(...arguments);
},
```

## willClearRender
### When
Called when a component is about to re-render but before any teardown has occurred.
### Use
A good time to tear down things that relied on DOM state.
### Example
Tear down manual observers attached to DOM state.
### Syntax
```javascript
willClearRender() {
    this._super(...arguments);
},
```