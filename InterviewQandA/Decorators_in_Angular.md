# Decorators in Angular

Angular uses decorators to attach metadata to classes, methods, properties, and parameters. These decorators tell Angular how to treat the thing they’re decorating.

---

## 1. Class Decorators

These define Angular building blocks.

### **@Component**
Defines a component with template, styles, and selector.

### **@Directive**
Defines a directive (structural or attribute).

### **@Pipe**
Defines a custom pipe.

### **@NgModule**
Defines an Angular module.

### **@Injectable**
Marks a class as available for dependency injection.

---

## 2. Property Decorators

Used inside classes to mark properties for Angular binding or DI.

### **@Input**
Receives data from a parent component.

### **@Output**
Emits events to a parent component.

### **@HostBinding**
Binds a property to a host element property or attribute.

### **@ContentChild**
Gets a reference to projected content (single element).

### **@ContentChildren**
Gets multiple projected content elements.

### **@ViewChild**
Gets a reference to a child component or DOM element.

### **@ViewChildren**
Gets multiple child components or DOM elements.

---

## 3. Method Decorators

### **@HostListener**
Listens to events on the host element.

---

## 4. Parameter Decorators

Used for dependency injection.

### **@Inject**
Explicitly specifies the provider token.

### **@Optional**
Marks a dependency as optional.

### **@Self**
Resolve dependency only from the current injector.

### **@SkipSelf**
Skip the current injector and look in parent injectors.

### **@Host**
Resolve dependency from the host element’s injector.

---

## 5. Routing Decorators (Legacy / Less Common)

> Modern Angular prefers functional guards, but these may still appear in older codebases.

### **@CanActivate**
Route guard for entering a route.

### **@CanDeactivate**
Guard for leaving a route.

### **@Resolve**
Pre-fetch data before route activation.

---

## 6. Advanced / Rare Decorators

### **@Attribute**
Injects a static attribute value from the host element.

---

## Summary Table

| Decorator | Purpose |
|----------|---------|
| **@Component** | Create a component |
| **@Directive** | Create a directive |
| **@Pipe** | Create a pipe |
| **@NgModule** | Create a module |
| **@Injectable** | Register a service for DI |
| **@Input** | Parent → Child data |
| **@Output** | Child → Parent events |
| **@ViewChild / @ViewChildren** | Access template children |
| **@ContentChild / @ContentChildren** | Access projected content |
| **@HostBinding** | Bind to host element |
| **@HostListener** | Listen to host events |
| **@Inject** | Explicit DI token |
| **@Optional / @Self / @SkipSelf / @Host** | DI resolution control |

