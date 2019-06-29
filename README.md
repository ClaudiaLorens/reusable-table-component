# Instructions to run the app:

Reading this document will help you to run the app easily.
This app uses Vue.js. First of all, please make sure you have node and Vue installed.

## Installation

After cloning or downloading the project, go to the project folder in your command line and  run the following command:

```
npm install
```

## Running the app

Once everything is installed, run the following command to see the app in your localhost:

```
npm run serve
```

Just click the link to see the app in your localhost, by default: http://localhost:8080/

Thanks for downloading it!


# Instructions to use the table:

This table component is still ongoing. It is highly reusable and customizable, to make use of it you just need to instantiate the component passing 3 arrays:

1.- Array of objects (tableList) you want to show in your table.
2.- Array of table header's name (tableHeaders), the names you want to show at the top of the table.
3.- Array properties (properties), the object's properties you want to show in your table.

You can use the "slot" to include some html or icons for the last column if you want so.


That's it! Hope this component makes your life easier.