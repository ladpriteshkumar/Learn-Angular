## Explain Change Detection in Angular
Change Detection in Angular is the mechanism that keeps the component’s data (model) in sync with the DOM (view).  

Whenever the application state changes—due to user actions, async operations, or events—Angular runs change detection to update the UI accordingly.

### How Angular Change Detection Works
Angular maintains a component tree, and each component has its own change detector.
When change detection runs, Angular walks this tree and checks if any bindings have changed.

Change detection is triggered by:

- DOM events (click, input)
- HTTP responses / Promises / Observables
- Timers (setTimeout, setInterval)
- Signals (Angular 16+)
- Manual triggers using ChangeDetectorRef
