# Custom ion-icon not migrated to standalone
This is a repo to reproduce the problem for the issue https://github.com/ionic-team/ionic-angular-standalone-codemods/issues/52

# To install please:

- make sure to install nodejs and ionic cli (see details in Ionic Info output below)
- issue `npm install`
- issue `ionic serve` to start the app
- open the browser and navigate to `http://localhost:8100/`
NOTE: the app is a simple Ionic app with a single page and a custom icon displayed on it.

# To reproduce the problem:

- execute migration according to the [migration instructions](https://github.com/ionic-team/ionic-angular-standalone-codemods?tab=readme-ov-file#usage)
NOTE: after the migration complete the app will not build. If `home.page.ts` is opened in IDE, the below typescript error will be displayed:
```
Module '"ionicons/icons"' has no exported member 'customFingerPrint'.
```
Please also note that `HomePage` compoment is not standalone anymore and the `@Component` decorator is missing the `standalone: true` property. The `HomePageModule` is still present in the `home.module.ts` file.

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
