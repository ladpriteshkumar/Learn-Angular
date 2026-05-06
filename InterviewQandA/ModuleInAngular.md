# What is a Module in Angular?

**A module in Angular is a class decorated with `@NgModule` that groups related components, directives, pipes, and services into a cohesive functional block.**

---

## 📌 What an Angular Module (NgModule) *is*

An **NgModule** is a core building block in Angular. It acts as a **container** that organizes parts of your application so Angular knows:

- **Which components, directives, and pipes belong to this module**  
  (`declarations`)
- **Which external modules it depends on**  
  (`imports`)
- **What it makes available to other modules**  
  (`exports`)
- **Which services it provides**  
  (`providers`)
- **Which component should bootstrap the app**  
  (`bootstrap`, only in root module)

Every Angular app has at least one module: **AppModule**.

---

## 🎯 Why Modules Matter

Angular modules help you:

- Organize your app into feature areas  
- Control visibility of components and services  
- Manage dependencies cleanly  
- Enable **lazy loading** for performance  
- Integrate external Angular libraries (e.g., `FormsModule`, `RouterModule`)  

---

## 🧩 Example of an NgModule

```ts
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule {}
```
## 📚 Key Metadata Properties

| Property | Purpose |
| --- | --- |
| **declarations** | Components, directives, pipes owned by this module |
| **imports** | Other modules whose exported classes are needed here |
| **exports** | What this module exposes to other modules |
| **providers** | Services available via dependency injection |
| **bootstrap** | Root component to launch the app (root module only) |


## 🔎 Note on Standalone Components
Angular now encourages standalone components for new development, but NgModules remain essential for understanding existing applications.
