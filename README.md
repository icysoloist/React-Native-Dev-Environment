# React-Native-Dev-Environment
All the necessary files to configure your development environment for a brand new React Native project.

## Instructions for Setup
Because a React Native project has alot of configuration files (for both iOS/Android), it is difficult to rename the project, its dependencies, and it's package names. For that reason, it is best to start a new project from scratch, and then copy over files needed to configure the rest of the environment.

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
