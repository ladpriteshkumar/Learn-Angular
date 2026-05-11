# Reactivity in Angular
Reactivity in Angular is the mechanism that automatically keeps the UI in sync with your application state. When data changes, Angular detects that change and updates only the relevant parts of the DOM, In Angular, this is mainly implemented through change detection (traditionally powered by Zone.js) and, in modern Angular, through Signals 

“In Angular, reactivity is essentially its change detection system—how Angular knows data changed and when to update the view.”

## Traditional reactivity: Zone.js and change detection

### How Zone.js works (classic Angular)
- **Zone.js role:**  
Angular runs your app inside a special zone (NgZone) that monkey‑patches async APIs like setTimeout, Promises, HTTP calls, and DOM events. 

- **Triggering change detection:**  
Whenever one of these async operations completes (click, HTTP response, timer, etc.), Zone.js notifies Angular: “something happened.” Angular then runs a change detection cycle.

- **Change detection pass:**  
Angular walks the component tree from the root, evaluates template bindings, and updates the DOM where values changed. This is the default, “it just works” reactivity model.


### Pros and cons (good to mention in interviews)
- **Pros:**   
Easy mental model: you change a variable, the UI updates.   
No manual wiring: Angular automatically reacts to async events.

- **Cons:**   
Potentially wasteful: a single click can trigger checks across the entire component tree, even if most components didn’t change.   
Performance risk in large apps: unnecessary checks can become a bottleneck.

```
“By default, Angular’s reactivity is Zone.js‑driven: any async event can trigger a full tree change detection pass.”
```



## 3. OnPush: more controlled reactivity on top of Zone.js
Even before Signals, Angular gave us ChangeDetectionStrategy.OnPush to make reactivity more selective.

### Default vs OnPush:   
**Default:** component is checked on every change detection cycle.   
**OnPush:** component is checked only when specific triggers occur.

### OnPush triggers:   
- @Input() reference changes (not mutation, but a new reference).   
- DOM event from the component or its children.   
- async pipe emits a new value.   
- Manual trigger via ChangeDetectorRef.markForCheck().

```
“OnPush doesn’t change how Angular detects changes, but when it runs detection for a component. It narrows reactivity to specific triggers, which improves performance.”
```


Modern reactivity: Angular Signals


# Modern Reactivity in Angular: Signals

Angular Signals introduce a new, fine‑grained reactivity model that makes UI updates more predictable, efficient, and explicit. Unlike Angular’s traditional Zone.js‑driven change detection, Signals update only the parts of the application that actually depend on the changed value.

Signals are the foundation of Angular’s modern reactive system and a key part of Angular’s move toward zoneless, high‑performance applications.

---

## What Are Signals?

A **Signal** is a reactive value that:

- Holds state  
- Notifies Angular when it changes  
- Automatically updates any consumers (templates, computed values, effects)

Signals are *pull‑based*: Angular tracks which consumers read a signal and updates only those consumers when the signal changes.

### Basic Example

```ts
import { signal } from '@angular/core';

export class CounterComponent {
  count = signal(0);

  increment() {
    this.count.set(this.count() + 1);
  }
}

