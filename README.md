# Angular

## What is Angular
Angular is one o the most powerful ```JavaSctipt``` framework to build single page application for both web and mobile 
- Angular follows components oriented design pattern to build web application

## What is a Component in Angular?
A component is the fundamental building block of the UI in angular application.

Modern Angular uses standalone components, meaning they can declare their own dependencies without needing an NgModule, which makes the architecture more lightweight and modular.

Components are the primary way Angular renders and updates the DOM efficiently.

### Components help you:

- Break your app into small, manageable pieces
- Reuse UI parts across pages
- Keep logic, layout, and styling organized
- Build scalable applications with clear structure

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
