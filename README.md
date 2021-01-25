# React-Native-Dev-Environment
All the necessary files to configure your development environment for a brand new React Native project.

## Instructions for Setup
Because a React Native project has a lot of configuration files (for both iOS/Android), it is difficult to rename the project, its dependencies, and its package names. For that reason, it is best to start a new project from scratch, and then copy over any files needed to configure the rest of the environment.

> The instructions below are tightly coupled with the assumption that you have read about [Setting Up A Development Environment](https://reactnative.dev/docs/environment-setup) in the React Native official docs.

### Step 1
Initialize a new React Native app with the command:\
`npx react-native init <app_name>`

If your project is using TypeScript, then it is best to install with a community preferred TypeScript template:\
`npx react-native init <app_name> --template react-native-template-typescript`

### Step 2
Setup dependencies for the project.
1) Delete `node_modules` and `yarn.lock`
2) Copy the `package.json` from this repo into the project (be sure to update the `name` property in this file)
3) Run `yarn install`

### Step 3
Copy over the environment configuration files.
- `tsconfig.json` : defines TypeScript compiler/configuration settings
- `metro.config.js` : configuration for Facebook's Metro bundler
- `jest.config.js` : Jest (testing library) config
- `.babelrc` : Babel (JSX transpiler) config. Be sure to remove/rename the existing `babel.config.js`
- `.prettierrc` : Prettier (code formatter) config. Be sure to remove/rename the existing `prettierrc.js`
- `.eslintrc` : ESLint (code linter) config. Be sure to remove/rename the existing `eslintrc.js`
- `.prettierignore` : Defines files to not be formatted by Prettier (similar to `.gitignore`)
- `index.js` : root file for the project

> If the linters/formatters are throwing red squillies even after all files have been copied over, try reloading the developer window (CTRL+SHIFT+P in VSCode)

### Step 4 (for VSCode users only)
#### TODO - specify VSCode settings.json edits

## Instructions for running the app
In order to run, debug, and test a React Native app, you will need to have an emulator running. Below are instructions for each platform.

### Android/Android Studio
The [React Native docs](https://reactnative.dev/docs/environment-setup) have a thorough guide to installing Android Studio and any emulators.
Before trying to run the app, ensure the project is open in Android Studio.

### iOS/XCode
#### TODO - instructions for iOS/XCode

### Run the damn thing!
You will need to have Metro Bundler running first:
`yarn run start` (which is shorthand for `npx react-native start`)
