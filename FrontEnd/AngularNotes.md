# Angular Tutorial

Welcome to the Angular tutorial! This guide will help you get started with Angular, a popular framework for building web applications.

## Table of Contents
1. [Introduction](#introduction)
2. [Setup](#setup)
3. [Creating a New Project](#creating-a-new-project)
4. [Components](#components)
5. [Services](#services)
6. [Routing](#routing)
7. [Data Binding](#data-binding)
8. [HTTP Client](#http-client)
9. [Conclusion](#conclusion)

## Introduction
Angular is a platform for building mobile and desktop web applications. It provides a robust framework for developing single-page applications (SPAs) with a rich user interface.

## Setup
To get started with Angular, you need to have Node.js and npm installed on your machine. You can download them from [Node.js](https://nodejs.org/).

Next, install the Angular CLI globally using npm:
```bash
npm install -g @angular/cli
```

## Creating a New Project
Create a new Angular project using the Angular CLI:
```bash
ng new my-angular-app
cd my-angular-app
```
Run the development server:
```bash
ng serve
```
Open your browser and navigate to `http://localhost:4200/` to see your new Angular app in action.

## Components
Components are the building blocks of an Angular application. Create a new component using the Angular CLI:
```bash
ng generate component my-component
```
This command will create a new component with the necessary files and update the module.

## Services
Services are used to share data and functionality across components. Create a new service using the Angular CLI:
```bash
ng generate service my-service
```
Inject the service into a component to use it:
```typescript
constructor(private myService: MyService) { }
```

## Routing
Routing allows you to navigate between different views in your application. Define routes in the `app-routing.module.ts` file:
```typescript
const routes: Routes = [
    { path: 'home', component: HomeComponent },
    { path: 'about', component: AboutComponent },
];
```
Import the `RouterModule` and add it to the `imports` array in your module:
```typescript
imports: [RouterModule.forRoot(routes)]
```

## Data Binding
Angular supports various types of data binding:
- **Interpolation**: `{{ value }}`
- **Property Binding**: `[property]="value"`
- **Event Binding**: `(event)="handler"`
- **Two-way Binding**: `[(ngModel)]="value"`

## HTTP Client
Use the `HttpClient` module to make HTTP requests. Import the module in your `app.module.ts`:
```typescript
import { HttpClientModule } from '@angular/common/http';

@NgModule({
    imports: [HttpClientModule]
})
export class AppModule { }
```
Inject the `HttpClient` service into your component or service:
```typescript
constructor(private http: HttpClient) { }

this.http.get('https://api.example.com/data')
    .subscribe(data => console.log(data));
```

## Conclusion
Congratulations! You have learned the basics of Angular. Continue exploring the Angular documentation and building your own applications.

Happy coding!