## What are decorators in Angular ?
Decorators are special functions in `TypeScript`, prefix with @symbol, that attach metadata to class, property, method and parameter.

In Angular, decorators tell the framework how to treat the class, property method and parameter based on decorator applied.


**There are four main types of decorator in Angular.**

## 1. Class Decorators
**`@Component`** Defines a component with template, styles, and selector.

**`@Directive`** Defines a directive (structural or attribute).

**`@Pipe`**

**`@NgModule`**

**`@Injectable`** Marks a class as available for dependency injection.

---

## 2. Property Decorators
**`@Input`** Receives data from a parent component.

**`@Output`** Emits events to a parent component.

**`@HostBinding`** Binds a property to a host element property or attribute.

**`@ContentChild`** Gets a reference to projected content (single element).

**`@ContentChildren`** Gets multiple projected content elements.

**`@ViewChild`** Gets a reference to a child component or DOM element.

**`@ViewChildren`** Gets multiple child components or DOM elements.

---

## 3. Method Decorators

**`@HostListener`** Listens to events on the host element.

---

## 4. Parameter Decorators

**`@Inject`** Explicitly specifies the provider token.

**`@Optional`** Marks a dependency as optional.

**`@Self`** Resolve dependency only from the current injector.

**`@SkipSelf`** Skip the current injector and look in parent injectors.

**`@Host`** Resolve dependency from the host element’s injector.

