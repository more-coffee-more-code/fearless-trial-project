# Purple Cow Project
#### This web app now only allows the user to click on a button that displays the number of total hits the Counter API (https://countapi.xyz/) has received, but it also keeps track of the number of times the user has clicked on the button. The app was built using Vue.js, HTML, CSS, SASS, JavaScript, and BEM.

## Here is a simple flow chart to demonstrate how it works
<img src="./src/assets/flowchart.jpg" alt="">

## Project setup and configuration
#### Before attempting to run the application, please take a second to install its dependencies. This can be accomplished by running the following command:
```
npm install
```
#### After installing the dependencies you will be able to fire up the application. Use the command below. Please not the default port the application will run on is `:8080`:  
```
npm run serve
```
#### If you wish to change the port number the application runs on, then run this command:
```
npm run serve -- --port 3000
```
#### To compile and minify the application for production run the following command:
```
npm run build
```
#### To lint and fix files (indents, spacing, etc) run this command:
```
npm run lint
```

## Future updates to this project
#### After analyzing the application and receiving feedback from users, I will be adding a lifecycle method `beforeMount` to ping the API and populate the `Total Hits` indicator before the first button click. Having a prepopulated indicator makes more sense from a UX perspective. Here is the code snippet I would add:
```
beforeMount() {
  this.getDataFromApi()
}
```

#### Another change I would make is to add a global count variable. As of now the parent component holds the `count` data property and updates it's children with the new value. However, it might be cleaner for the parent and children components to read from a global store.


