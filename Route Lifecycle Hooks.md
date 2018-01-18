## willTransition
#### When
Fired with the transmission argument when Ember starts constructing the route transmission
#### Use
Stop the transmission from occurring
#### Example
Display a prompt if the user navigates away from a form with unsubmitted data.
#### Syntax
```javascript
willTransition() {
    this._super(...arguments);
},
```
******
## beforeModel
#### When
Triggered with a single transition argument BEFORE execution of the current routes model.
#### Use
Primarily to redirect to another route before model instantiation OR for triggering some async operations before model is resolved.
#### Example
if an unauthenticated user attempts an auth route we can save the transistion at this point and trigger a login.
#### Syntax
```javascript
beforeModel() {
    this._super(...arguments);
},
```
******
## model
#### When
Once we have confirmed that this is the correct model for the route
#### Use
Called with params and transition args to convert the URL into the correct model for the context.
#### Syntax
```javascript
model() {
    this._super(...arguments);
},
```
******
## afterModel
#### When
Immediately after the routes model has been resolved
#### Use
Good place to run logic that requires info from the current model
#### Example
Routing to a child route that requires the ID from the model, eg. path: '/:post_id'
#### Syntax
```javascript
afterModel() {
    this._super(...arguments);
},
```
******
## redirect
#### When
Called with the model and transition args. Nearly identical to afterModel(), The main difference is that at the point redirect() is called the route should be considered "active"
#### Use
Good place to run logic that requires info from the current model
#### Example
same as afterModel()
#### Syntax
```javascript
redirect() {
    this._super(...arguments);
},
```
******
## deactivate
#### When
Triggered when the router completely exits a route
#### Use
Any work needed immediately before exiting a route
#### Example
Trigger analytics
#### Syntax
```javascript
deactivate() {
    this._super(...arguments);
},
```
******
## activate
#### When
Triggered when the router enters a new route
#### Use
Any work needed immediately on a route being triggered
#### Example
Trigger analytics
#### Syntax
```javascript
activate() {
    this._super(...arguments);
},
```
******
## setupController
#### When
Called with the current route controller and the current model.
#### Use
Renders the routes template, configured with the current controller for the route.
#### Syntax
```javascript
() {
    this._super(...arguments);
},
```
******
## renderTemplate
#### When
Called with the current route controller and the current model.
#### Use
Renders the routes template, configured with the current controller for the route.
#### Syntax
```javascript
renderTemplate() {
    this._super(...arguments);
},
```
******
## didTransistion
#### When
When the transistion has successfully completed.
#### Use
Logic running immediately after transistion has completed
#### Example
Analytics, setting/resetting component state
#### Syntax
```javascript
didTransistion() {
    this._super(...arguments);
},
```
******