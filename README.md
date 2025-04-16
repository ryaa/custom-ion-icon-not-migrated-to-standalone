# Custom ion-icon not migrated to standalone
This is a repo to reproduce the problem for the issue

# To install please:

- make sure to install nodejs and ionic cli (see details in Ionic Info output below)
- issue `npm install`
- issue `ionic serve` to start the app
- open the browser and navigate to `http://localhost:8100/`
NOTE: the app is a simple Ionic app with a single page and a custom icon displayed on it.

# To reproduce the problem:

- execute migration according to the [migration instructions](https://github.com/ionic-team/ionic-angular-standalone-codemods?tab=readme-ov-file#usage)


# Ionic Info output

```
Ionic:

   Ionic CLI                     : 7.2.0 (/Users/alexryltsov/.nvm/versions/node/v20.11.1/lib/node_modules/@ionic/cli)
   Ionic Framework               : @ionic/angular 8.5.4
   @angular-devkit/build-angular : 19.2.7
   @angular-devkit/schematics    : 19.2.7
   @angular/cli                  : 19.2.7
   @ionic/angular-toolkit        : 12.2.0

Capacitor:

   Capacitor CLI      : 7.2.0
   @capacitor/android : not installed
   @capacitor/core    : 7.2.0
   @capacitor/ios     : not installed

Utility:

   cordova-res : not installed globally
   native-run  : 2.0.1

System:

   NodeJS : v20.11.1 (/Users/alexryltsov/.nvm/versions/node/v20.11.1/bin/node)
   npm    : 10.5.0
   OS     : macOS Unknown
```
