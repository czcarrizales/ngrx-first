# MeanFirst

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 12.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

# Ngrx Setup

## Step 1
add schematics
## Command
```
ng add @ngrx/schematics@latest --defaultCollection
true
```
## Step 2
ng generate store
## Command
```
ng generate store AppState --root --module app.module.ts --state-path store --state-interface AppState
```

## Step 3
add ngrx dependencies
*use git bash
## Command
```
npm install @ngrx/{store,effects,entity,store-devtools} --save
```

## Step 4
ng add action
## Command
```
ng g action store/user --group --api --flat false --skip-tests --prefix load --creators true
```

## Step 5
ng add reducer
## Command
```
ng g r store/user --creators true --flat false --group --module app.module.ts --skip-tests --api --reducers index.ts
```