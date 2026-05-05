# Templates and Data Binding in Angular

## 1. Templates in Angular
A **template** is the HTML (enhanced with Angular syntax) that defines the user interface of a component. It is connected to the component class, which provides data and behavior.

Templates can include:

- Standard HTML
- Angular features:
  - Interpolation (`{{ }}`)
  - Property binding (`[property]`)
  - Event binding (`(event)`)
  - Structural directives (`*ngIf`, `*ngFor`)
  - Template reference variables (`#var`)
  - Pipes (`| date`, `| uppercase`)

### Example Template
```html
<h2>{{ title }}</h2>
<p>Welcome, {{ userName }}</p>
<button (click)="logout()">Logout</button>
```

---

## 2. Data Binding in Angular
**Data binding** connects the component (TypeScript class) with the template (HTML view).  
It keeps the UI and data in sync automatically.

Angular supports four main types of data binding:

---

### 2.1 Interpolation (One-way: Component → Template)
Displays dynamic text.

```html
<p>Hello {{ userName }}</p>
```

---

### 2.2 Property Binding (One-way: Component → DOM)
Binds values to DOM properties.

```html
<img [src]="profileImageUrl">
<button [disabled]="!isValid">Submit</button>
```

---

### 2.3 Event Binding (One-way: DOM → Component)
Handles user actions.

```html
<button (click)="save()">Save</button>
```

With event object:

```html
<input (input)="onInput($event)">
```

---

### 2.4 Two-way Binding (Component ↔ Template)
Combines property and event binding.

```html
<input [(ngModel)]="userName">
```

---

## 3. Summary Table

| Binding Type | Direction | Syntax | Purpose |
|--------------|-----------|--------|---------|
| Interpolation | Component → Template | `{{ value }}` | Display dynamic text |
| Property Binding | Component → DOM | `[property]="value"` | Bind DOM properties |
| Event Binding | DOM → Component | `(event)="handler()"` | Handle user actions |
| Two-way Binding | Both ways | `[(ngModel)]="value"` | Sync UI and component |
