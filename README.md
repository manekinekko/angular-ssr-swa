# Angular Server Side Rendering on Azure Static Web Apps

This project was generated with [Angular CLI](https://github.com/angular/angular-cli).

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

# Deploying to Azure Static Web Apps

Follow the [Quickstart](https://bit.ly/2ABy9Cb) guide for Azure Static Web Apps and use the following configuration:

![screenshot-1589980551002](https://user-images.githubusercontent.com/1699357/82451694-a3202000-9aae-11ea-813a-35db0092b9df.png)

![screenshot-1589980574080](https://user-images.githubusercontent.com/1699357/82450911-95b66600-9aad-11ea-96d0-4576ff8ae07f.png)

![screenshot-1589980828843](https://user-images.githubusercontent.com/1699357/82450907-94853900-9aad-11ea-9e52-ee0b9e21b5c1.png)

By default, Azure Static Web Apps will execute the `npm run build` script. We need to update the [generated workflow file](https://github.com/manekinekko/angular-ssr-swa/blob/master/.github/workflows/azure-static-web-apps-blue-bay-00cc1f303.yml#L30) and explicitely run the `npm run prerender` script:

![angular-ssr-swa:azure-static-web-apps-blue-bay-00c](https://user-images.githubusercontent.com/1699357/82451219-f645a300-9aad-11ea-9e26-1db86ecc5aa3.png)

After saving and commiting our changes, another build will trigger and we should get the prerendered app deployed at the given URL for your app:

![screenshot-1589979864867](https://user-images.githubusercontent.com/1699357/82449287-496a2680-9aab-11ea-8c30-a7aa1db82deb.png)


