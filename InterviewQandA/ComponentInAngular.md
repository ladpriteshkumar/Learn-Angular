## What is a Component in Angular?
A component is the fundamental building block of the user interface(UI) in angular application.

Components are the primary way Angular renders and updates the DOM efficiently.

#### Components help you:
- Break your app into small, manageable pieces
- Reuse UI parts across pages
- Keep logic, layout, and styling organized
- Build scalable applications with clear structure

Modern Angular uses standalone components, meaning they can declare their own dependencies without needing an NgModule, which makes the architecture more lightweight and modular.

### what is @Component
**@Component** is the Angular **decorator** that marks a TypeScript class as a component and provides the metadata Angular needs to create, render, and manage that component.


### What @Component Actually Does
The @Component decorator is a function provided by Angular that attaches metadata to a class so Angular can treat it as a UI component. This metadata includes:

- selector — the custom HTML tag used to place the component
- template / templateUrl — the HTML that defines the view
- styles / styleUrls — CSS scoped to the component
- imports — dependencies for standalone components
- changeDetection, encapsulation, animations, and other advanced settings

According to Angular’s official documentation, the @Component decorator “marks a class as an Angular component and provides configuration metadata that determines how the component should be processed, instantiated, and used at runtime.”


### Minimal Example of component

```TypeScript
//File Name : Greet.ts
import { Component } from '@angular/core';

@Component({
  selector: 'greet',
  template: 'Hello {{name}}!'
})
export class Greet {
  name: string = 'World';
}
```

This example shows the three required pieces:

- selector: 'greet'
- template: inline HTML
- class: Greet, which holds logic

Angular uses this metadata to insert <greet></greet> into the DOM and render the template. 
