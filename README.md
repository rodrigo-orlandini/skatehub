# Skatehub

The idea of Skatehub was born to help the skateboarding community. Here, many resources will be available to provide facilities in the skater's day-to-day during his activity.

### Current features in the app
- Find and register good skateboarding spots;
- Find friends and see where they are skating;
- Create lists of tricks to try randomly.

![Good locations](/images/locations.png "Register good locations") ![Find friends](/images/friends.png "Make new friends") ![Randomize tricks](/images/randomize.png "Take tricks randomly")

### Application Workflow and Screens
If you want to see the preview of the application screens, follow the [Figma Project](https://www.figma.com/file/Q6XfaSNXks2sQihCKk5HNr/SkateHub?node-id=203%3A260)

![Application workflow](/images/workflow.png "Application workflow")

### Technology Details

To develop this application, it was used some **techonologies, patterns and architechture**.

The mobile application is built with *[React Native](https://reactnative.dev/)*, a *[cross-platform](https://en.wikipedia.org/wiki/Cross-platform_software#:~:text=In%20computing%2C%20cross%2Dplatform%20software,work%20in%20several%20computing%20platforms.&text=For%20example%2C%20a%20cross%2Dplatform,Windows%2C%20Linux%2C%20and%20macOS.)* *[Javascript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)* tool that allows you to create **native apps**. However, the application was coded with a "typed version" of Javascript, the *[Typescript](https://www.typescriptlang.org/)*, and the *[Container-View](https://dev.to/ornio/container-view-pattern-in-react-inc-hooks-5404)* design pattern was used for components and screens.

Some of packages/resources that were used in the **frontend**:
- **Async Storage** for Local Storage;
- **Axios** for HTTP Requests;
- **Lottie** for animations;
- **React Navigation** (Native Stack and Drawer);
- **Redux** to work with the application data.

In addition to the frontend, there is our backend. It was made a *[RESTful API](https://pt.wikipedia.org/wiki/REST)* using *[Flask](https://flask.palletsprojects.com/en/2.0.x/)*, a micro-framework for *[Python](https://www.python.org/)*. With that, our app is able to process and manage database information.

The both parts of the application (Frontend and Backend) has tests. The React Native application use *[Jest](https://jestjs.io/)* to write tests and in Flask application, while the Flask application use *[Pytest library](https://docs.pytest.org/en/7.1.x/)*.
The Frontend tests are structured as below:
- **Unit testing** in view and container components;
- **Integration testing** in the screens behavior.
And the Backend tests works as below:
- **Unit testing** to database models and utility functions;
- **Integration testing** for passing and receiving data from API's endpoints.

Some of packages/resources that were used in the **backend**:
- **Flask RESTful** to configure API with the REST principles
- **Flask JWT Extended** for JSON Web Tokens and authorization process
- **Flask Migrate** to do database migrations
- **Marshmallow** for data serialization
- **Python Dotenv** to help with environment variables
- **SMTPlib** to send emails
- **SQLAlchemy** as an ORM to communicate with database
- **UWSGI** as a server

In the application, the folder structure was elaborated to **split out the responsabilities** of each one piece of code. The current folder structure is divided into:

- **/assets:** Here are images, icons and fonts;
- **/components:** In this folder are only the components that are used in more than one screen of the application;
- **/models:** To create data models as a type;
- **/redux:** To configure redux, actions and reducers;
- **/routes:** To configure navigators, routes and navigation components, like Header, Drawer Content, etc.;
- **/screens:** All the screens are here, together the components of own screen;
- **/services:** The API configuration are here, in addition to the all calls to her;
- **/styles:** At last but not least, here are the styles that used in the entire application, like Typography, Colors, Sizes, etc.

### Development Steps

If you want to follow the development steeps further and see future ideas for the app, go to project dashboard in [Trello](https://trello.com/b/APwg8K3d/skatehub).
