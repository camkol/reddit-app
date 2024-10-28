# Instructions

## Table of Contents

- [Overview](#overview)
  - [Build Your Own Reddit App](#build-your-own-reddit-app)
  - [Example Project](#example-project)
  - [Project Requirements](#project-requirements)
- [Setup](#setup)
  - [Going off platform](#going-off-platform)
  - [Reddit API](#reddit-api)
- [Resources](#resources)
  - [Debugging Tips + Helpful Resources](#debugging-tips--helpful-resources)
  - [Example Code](#example-code)
- [Project Tasks](#project-tasks)
  - [Plan your project](#plan-your-project)
  - [Wireframe your application](#wireframe-your-application)
  - [Create files and run it locally](#create-files-and-run-it-locally)
  - [Version control](#version-control)
  - [Build the components](#build-the-components)
  - [Add Reddit data](#add-reddit-data)
  - [Publish to the web](#publish-to-the-web)
  - [Next steps](#next-steps)

## Overview

### Build Your Own Reddit App

For this project, you will build an application for [Reddit](https://www.reddit.com/) using everything you’ve learned, including React and Redux. Reddit is a website where people share links to articles, media and other things on the web. The Reddit API provides data which you will integrate into your application. The application will allow users to view and search posts and comments provided by the API.

### Example Project

![](./reddit-client-loading-slow.webp)
[Completed project sample](https://reddit-client.netlify.app/)

### Project Requirements:

- Build the application using React and Redux
- Version control your application with Git and host the repository on GitHub
- Use a project management tool (GitHub Projects, Trello, etc.) to plan your work
- Write a README (using Markdown) that documents your project including:
  - Wireframes
  - Technologies used
  - Features
  - Future work
- Write unit tests for your components using Jest and Enzyme
- Write end-to-end tests for your application
- Users can use the application on any device (desktop to mobile)
- Users can use the application on any modern browser
- Users can access your application at a URL
- Users see an initial view of the data when first visiting the app
- Users can search the data using terms
- Users can filter the data based on categories that are predefined
- Users are shown a detailed view (modal or new page/route) when they select an item
- Users are delighted with a cohesive design system
- Users are delighted with animations and transitions
- Users are able to leave an error state
- Get 90+ scores on [Lighthouse](https://pagespeed.web.dev/)
  - We understand you cannot control how media assets like videos and images are sent to the client. It is okay to have a score below 90 for Performance if they are related to the media from Reddit.
- OPTIONAL: [Get a custom domain name and use it for your application](https://www.codecademy.com/courses/make-a-website/lessons/setting-up-your-domain/exercises/hosting-your-site)
- OPTIONAL: Set up a CI/CD workflow to automatically deploy your application when the master branch in the repository changes
- OPTIONAL: Make your application a progressive web app
  Prerequisites:
- HTML
- CSS
- JavaScript
- React
- Redux
- Jest and Selenium
- Git and GitHub
- Command line and file navigation
- Wireframing

## Setup

### Going off platform

You will be doing this project outside of the Codecademy platform, on your own computer.

For this particular project, you will be using your own text editor (we suggest [VS Code](https://code.visualstudio.com/download)) and Git version control. If you need help setting up your text editor, read our [article about setting up a text editor for web development](https://www.codecademy.com/article/visual-studio-code). If you need a refresher on how to work with Git for version control, [review the Git lesson](https://www.codecademy.com/enrolled/courses/learn-git) or look at this [cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf).

### Reddit API

For this project, we will be using the [Reddit JSON API](https://github.com/reddit-archive/reddit/wiki/JSON). There is no maintained documentation but the API is simple enough to use. We will provide you with some pointers on how to use it.

Note that Reddit has 2 APIs: the [official API](https://www.reddit.com/dev/api/) and an [undocumented JSON API](https://github.com/reddit-archive/reddit/wiki/JSON). You are welcome to use either APIs but we recommend using the JSON API because it doesn’t require an OAuth workflow. Using the JSON API does have limitations such as no write operations. For the purposes of this project, we find the JSON API adequate.

You can take any Reddit URL, add .json at the end of it, and get JSON. For example, if you want to get the Popular page data in JSON:

- Original URL: https://www.reddit.com/r/popular/
- JSON URL: https://www.reddit.com/r/popular.json

If you want to search for “cake recipes”:

- Original URL: https://www.reddit.com/search?q=cake%20recipes
- JSON URL: https://www.reddit.com/search.json?q=cake%20recipes

Notice here you didn’t add `.json` at the end of the URL. You actually added it before the start of the query string. Refer to [this article](https://www.quora.com/What-are-the-parts-of-a-URL) for a breakdown of the structure of a URL.

The Reddit API will return some user content (comments) in Markdown. You should find a way to display the Markdown in your application.

**Note**: As of July 01, 2023, free use of Reddit APIs is [limited to 10 queries per minute](https://www.reddit.com/r/reddit/comments/145bram/addressing_the_community_about_changes_to_our_api/). If you begin to hit the rate limit while developing this app, subsequent queries may fail until the timer resets. You’ll need to consider how to address this programmatically.

## Resources

### Debugging Tips + Helpful Resources

Feeling stuck? Try the following:

- _Google your question:_ oftentimes, someone has had the same question as you! Check out websites like StackOverflow and Quora to see how other folks have found solutions.
- _Read the documentation:_ make sure to carefully read through the documentation for any languages and libraries that you are using. Oftentimes they’ll have examples of what you’re looking for!
- _Rubber ducking:_ try to explain a problem to a friend or co-worker. Oftentimes you’ll figure out the solution as you’re trying to explain it. And if not, getting another pair of eyes on your code can be helpful.

Check out these helpful resources:

- [Thinking About Errors in Your Code Differently](https://www.codecademy.com/content-items/673d70052fe5627f2222ab7840b4c5db)
- [Intro to Chrome Devtools](https://www.codecademy.com/content-items/8e57b181e3c4a62b70476bd76ab11624)
- [CSS Visual Rules in Chrome Inspector](https://www.codecademy.com/content-items/73ce848773660b8f73086a073113c3fe)
- [Documentation and Research](https://www.codecademy.com/content-items/8219be05381030feb2d9530fedb457fd/exercises/overview)
- [Debugging JavaScript Code](https://www.codecademy.com/content-items/e8a7f4f36eae1c4ee642af3cea4bfb4a/exercises/debugging-overview)
- [React Developer Tools](https://www.codecademy.com/paths/build-web-apps-with-react/tracks/bwa-intro-to-react/modules/ravenous-part-one/informationals/ready-react-developer-tools)
- [Redux DevTools Extension](https://www.codecademy.com/content-items/698c535e3cdf6ce8484bd34138341767)

### Example Code

Want to see an example of how someone else has completed this project? Click this [link](https://static-assets.codecademy.com/Paths/front-end-career-path/reddit-client/reddit-client-master.zip?_gl=1*1h28et6*_gcl_au*MjAzOTk1NjcxOS4xNzI5Nzk3NzYz*_ga*NDAzMjc3NjIxMi4xNzI5Nzk3NzU5*_ga_3LRZM6TM9L*MTczMDExNzg0MC4xMi4xLjE3MzAxMjAwODIuNjAuMC4w) to download a zip file containing one example solution to this project. Remember: your project doesn’t have to look anything like this! It should be unique to your vision.

Here’s an example for inspiration:
![](./reddit-client-loading-slow.webp)

## Project Tasks

Keep track of your progress by dragging each task from "To Do" to "In Progress" to "Done" as you work on them. You can also click on a task to see more information about it.

To Do

### Plan your project

Visualize your end result. What is it built with? What can it do? Make sure that it satisfies all of the project objectives.

Make a timeline for yourself and avoid the temptation to build things that aren’t required. Setting firm boundaries and deadlines will keep you on track and prevent [scope creep](https://en.wikipedia.org/wiki/Scope_creep).

The following tasks will help you identify natural break points.

### Wireframe your application

Using pencil and paper, or a wireframing software of your choice, draft what you’d like your application to look like.

**Hint**

Think about what the main components of the site will be and how you would like to see them arranged on the page. You should also think about the user flow and design all of those states and transitions as well. Don’t forget about error states!

You should also think about:

- The application’s color palette
- How to break up your design into components
- How your application will look at different screen sizes

### Create files and run it locally

On your computer, create the files needed for your React application. Run your application locally to see what it looks like in the browser.

**Hint**

You can use [create-react-app](https://create-react-app.dev/) to start your React application. If you want to set up Redux automatically, you can use the [Redux flag](https://redux-toolkit.js.org/introduction/getting-started#using-create-react-app).

### Version control

Set up the folder you created previously to be a Git repository. Push the initial files to a repository on GitHub. You should be consistently committing your changes throughout the project. Make sure to have meaningful commit messages.

**Hint**

To initialize your Git repository, you can run the below code in your terminal, where application is the name of your project folder.

```node
git init application
```

If you want a refresher on the syntax, look back at the [Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf).

### Build the components

Based on your wireframes, start building your application with fake, local data. Remember to build reusable components and to keep your components small.
Other things to keep in mind:

- Your application should work for all screen sizes
- You are welcome to use libraries to help you accomplish features
- You should write unit tests and end-to-end tests where it makes sense

**Hint**

If you’re not sure what content to include, use this example as inspiration:
![](./reddit-client-loading-slow.webp)

Your project should not look exactly like this one, but it should help you get a sense of what you might want to include.

### Add Reddit data

Connect your application to the Reddit API.
When interacting with the API, don’t forget to handle error states.
Make sure you set up your app to handle errors related to the API rate limits (as mentioned in the **Setup** tab). See the Hint for ideas!

**Hint**

A few ways to work within the rate limits:

- cache the results of some successful queries, then show those when a query fails
- look for ways to reduce the overall number of queries being made
- provide a front-end error to the user that new data could not be loaded

### Publish to the web

Congratulations on building your application! Deploy what you’ve built and share it with the world!
Hint
There are many ways to deploy your application online, including GitHub Pages and Netlify.

### Next steps

Go back to the project requirements section and complete the optional requirements.
