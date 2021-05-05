Run Node.js scripts from the command line
The usual way to run a Node.js program is to run the node globally available command (once you install Node.js) and pass the name of the file you want to execute.

If your main Node.js application file is app.js, you can call it by typing:

node app.js

While running the command, make sure you are in the same directory which contains the app.js file.

*****************************************************************************************
An Express application#
Express is a very popular application framework for building and running Node.js applications. You can scaffold (create) a new Express application using the Express Generator tool. The Express Generator is shipped as an npm module and installed by using the npm command-line tool npm.

Tip: To test that you've got npm correctly installed on your computer, type npm --help from a terminal and you should see the usage documentation.

Install the Express Generator by running the following from a terminal:

npm install -g express-generator
The -g switch installs the Express Generator globally on your machine so you can run it from anywhere.

We can now scaffold a new Express application called myExpressApp by running:

express myExpressApp --view pug
This creates a new folder called myExpressApp with the contents of your application. The --view pug parameters tell the generator to use the pug template engine.

To install all of the application's dependencies (again shipped as npm modules), go to the new folder and execute npm install:

cd myExpressApp
npm install
At this point, we should test that our application runs. The generated Express application has a package.json file which includes a start script to run node ./bin/www. This will start the Node.js application running.

From a terminal in the Express application folder, run:

npm start
The Node.js web server will start and you can browse to http://localhost:3000 to see the running application.