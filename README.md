# symfony-react-web-app

## Prerequisites

Make sure that we have [Node.js](https://nodejs.org/en/) and [Yarn package manager](https://yarnpkg.com/lang/en/docs/install/) installed on  development machine. Lastly, we need to install [Composer](https://getcomposer.org/) to manage dependencies.

## What we will build with React and Symfony

This application represents a little bit of deviation from how Symfony as a framework traditionally works. From state management of data, to page rendering, and routing from one page to another, the approach that we will employ depends fully on using [React Router](https://reacttraining.com/react-router/web/) for routing and management of the state of the application. It differs by using the local state object within each React reusable component to store history, providing real-time responsiveness.

To fetch the list of users, we build a backend API with dummy data using Symfony. To fetch the list of posts, we make use of a fake online REST API for testing and prototyping named [JSONPlaceholder](https://jsonplaceholder.typicode.com/).

## Scaffolding the Symfony Application

We use Composer to quickly create a new Symfony application. 

## Running your React and Symfony App

To run the application and test its functionality ensure that both the Symfony and React application are currently running from separate terminals within project directory.

```bash
php bin/console server:run
```

We can test the backend API using [Postman](https://www.getpostman.com/). Try accessing the user list endpoint on http://localhost:8000/api/users. You will see the list of users as show here:


![](https://paper-attachments.dropbox.com/s_1265725ADB054532A55C0EFD08DF0FAB2CEE8562C503298703A715DFE50C9E5D_1563644901996_symfony-users.png)

And from the second terminal, run the following command to compile the React application and watch the JavaScript files for any changes:

```bash
yarn encore dev --watch
```

Navigate to `http://localhost:8000` to view the list of users:


![](https://paper-attachments.dropbox.com/s_1265725ADB054532A55C0EFD08DF0FAB2CEE8562C503298703A715DFE50C9E5D_1563647884397_list-users.png)


Next, click on **Posts** from the navigation bar to view the list of posts fetched from the [JSONPlaceholder](https://jsonplaceholder.typicode.com/):


![](https://paper-attachments.dropbox.com/s_1265725ADB054532A55C0EFD08DF0FAB2CEE8562C503298703A715DFE50C9E5D_1563647978911_post-list.png)
