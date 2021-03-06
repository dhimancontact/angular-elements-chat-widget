# Chat Widget built with Angular Elements

Angular Elements allows you to create Custom Elements (from the WebComponents spec) from Angular Components.

This means that those components can be used outside of an Angular app!

## Project Structure

The project is a standard Angular 6 project with a few additions:

```
src/app/element.module.ts   Module with the component to be used as Angular Element. Imported by App Module
src/main.element.ts         bootstrap the Element Module
src/polyfills.element.ts    polyfills for the Element Module
build-elements.js           script to generate the exported file and demo project
```

### Development

The component can be developed as any other Angular component: run `ng serve` and navigate to `http://localhost:4200/`.

## Build

To build the Angular Elements, there is a special npm run-script: `npm run build:elements`. This scripts invokes `ng build` with a couple of parameters
so it creates a build in `dist/element-build` that only contains `ElementModule`. 

After this build the `./build-elements.js` script creates the final js file and
demo project in `dist/elements`.
