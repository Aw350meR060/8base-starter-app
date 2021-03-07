# 8base Test Task

The purpose of this task is to learn about using 8base and make an impression of its functions, usability and any problems along the way.

## Impressions

Overall, 8base is an excellent platform for organising backend of web apps, although there were some mishaps in my experience and suggestions for its improvement, which are listed below. Web application's UI is intuitive and allows its user to manage all of the basic needs of an application's backend server and database. The documentation is written simply enough to be understandable by someone without practial experience with web developement (e.g. me :^) ), but not too trivially. I also appreciated the bits of non-formal text in the documentation.

## Specific feedback

Below is a list of specific problems and suggestions to 8base, which I encountered while doing the Quick Guide and organising CI/CD in my test project. These are sectioned by parts of the Quick Guide, but not separated by relation to the 8base itself or the documentation.

### Creating a workspace
- I've encountered a problem while trying to create a workspace - I just couldn't create one!I've tried to make several 8base accounts, login with github and google, but to no purpose. The app was displaying an error (something related to invalid login) after pushing the "create" button, and there was no workspace created. Luckily the problem vanished by itself on the next day.

### Data Builder
- This is more of an suggestion than a problem. In a completely new workspace, there are two buttons in the *'Data Builder'* page - *'New Table'* in the table tree and *'Add Table'* on the right part of the screen. It's a little misleading in my opinion, I think that there should be some uniformity in button names that basically perform the same task;
- In the Quick Guide ([p2.1](https://docs.8base.com/docs/getting-started/quick-start/#21-building-a-data-model)), in the description of the *'user'* field there is an typo - *'A notes **other**'*. I think it meant to be ***author***;
- In the Quick Guide ([p2.1](https://docs.8base.com/docs/getting-started/quick-start/#21-building-a-data-model)), in the options of the *'user*' field there is an typo - the relation settings are mixed up. As it is, they build a *many-to-one* relationship, instead of *one-to-many*.

### API Explorer & GraphQL
- The GraphQL sript for creating dummy records provided in the Quick Guide ([p2.1](https://docs.8base.com/docs/getting-started/quick-start/#21-building-a-data-model)), appears to be not working - it causes errors related to using arrays (***Expected type User_NoteCreateInput, found \[...\].***) and *'count'* (***Cannot query field "count" on type "Note".***);

### Setting up the Client
- While trying to run the React.js starter app, I've encountered a dependancy error which prevented me to start the client. I've bypassed this by adding *'SKIP_PREFLIGHT_CHECK=true'* to the *'.env'* file. There was no such thing in the Vue.js client;
- I couldn't make the *Sign In* button load the authorizaton screen in both of starter apps, despite the correct data in the *'.env'* files. After pressing the button there is an ***'An error was encountered with the requested page.'*** message. The link in the address bar suggests that there was an ***invalid request*** of some sorts.

### CI/CD:
- I didn't really understand the purpose of environments. At first I thought it was something alike git branches, but in my experience there were no changes after changing one - the structure of the workspace folder stayed the same, regardless of differences in environments (8base.yml and other files). I think it is some error on my side, but I wanted to elaborate on that.

### Documentation (outside of QS)
- While researching [Custom Functions](https://docs.8base.com/docs/8base-console/custom-functions/) in the documentation, I've found that links  to the Custom Function Types pages redirect you to nonexistent ones.
