# Dynamic Learning

## Overview

Dynamic Learning is meant to be an online platform where teachers and programmers collaborate to create and share STEM lessons which makes use of interactive visualisations created in p5.js. The main objective in GSoC 2018 was to lay down a basic structure of the app which will act as a foundation for future developments and will provide an idea of what the app is all about to the teacher community and future contributors.

The three core objectives of the web app are-

1) Teachers should be able to create, present, save and share lessons which make use of interactive visualisations.
2) Teachers should be able to collaborate with programmers to produce new visualisations.
3) Students should be able to view the video lessons prepared by teachers and should be able to use the simulations
the same time they watch it.

## Link to the working webapp

http://dynamiclearning.io

## Frameworks used

The webapp is build on top of full stack Javascript framework Meteor.js along with React.js. Meteor.js comes with inbuilt Mongo DB database which used in the app. Semantic UI React is used for obtaining styled ui components used throughout for making the ui of the app.

## Link to Github repo

https://github.com/JithinKS97/dynamic-learning-app

## Main react components

Below are the main React Components of the app and much of the work in GSoC 2018 was focused on the development
of these react components. These main react page components can be found in 'client/ui/pages'.

The routes of each of the pages can be found in the 'clients/routes' directory. Detailed documentation for each
of the components are provided in the component's js files.

### 1) Lessonplan creator

Component - CreateLessonPlan

This is the area where teachers create the lesson. It is basically a drawing app on which simulations can be embedded and notes can be added. Each lessonplan consists of a sequence slides which is implemented as an array. Each element in the array consists of a note of string type and an array of simulations.

Each simulation is an iframe which is obtained from the online p5 text editor export feature.

### 2) Login and Signup components

Components - Login, Signup

The login and sign up features are made by making use of the inbuilt authentication tools in Meteor.

### 3) The lessonplan, simulations, lessons organization

Components - LessonplansDirectories, LessonsDirectories, SimsDirectories

React Sortable tree component (https://github.com/frontend-collective/react-sortable-tree) is used for building the interface for the organization of lessonplans, lessons and the uploaded simulations.

### 4) Request Forum

Component - Request

For each lessonplan, a request forum can be created by the teacher where a request for a new simulation can be made. These requests are visible to all the other users of the app and anyone can participate in the discussion for the development of a new simulation.

### 5) Sharing of lessonplans, lessons and simulations

Components - SharedSims, SharedLessonPlans, SharedLessons

The users can share lessonplans, lessons and the simulations with the other users if they want. I've used the meteor easy search component for implementing the search (https://github.com/matteodem/meteor-easy-search)

#### Above are the main React Components of the app and the you can find the other React Components in the'client/ui/components' folder.

I've provided necessary documentation in the component js file itself in all the areas where I felt like clarifications are necessary.

## Features that can be added

1) In this year's GSoC, my main target was to develop the overall basic structure of the application on top of which further development can be done. I haven't given much emphasis on the design aspects and didn't go much into the styling (The Components of Semantic UI React comes up with the essential styles that are needed). So before the release, we should come up with a design theme for the whole app.

2) Unit testing - Apart from some server side tests, no tests have been written. I think we should write enough test cases for the server side and client side code, so that the future contributors can add features without breaking the existing code.

3) Enhancing the Discussion forum. The forums area can be enhanced by providing more features like providing Avatars for each users and the ability to reply to the comments, voting for the comments etc.

4) Adding Comments forum for the lessons.

5) Profile page for the users and notifications.

6) Login and Signup using Github, Google, email verification, password recovery.

7) Smoothening of the canvas strokes. At present, we don't do any sort of smoothening for the drawings we make in the canvas, so the annotations we create are not so smooth. If we can implement some sort of smoothening algorithm, the annotations will be more beautiful.


For feature enhancements, bug reports and contributions

You can email me to jithunni.ks@gmail.com or you can create an issue in the repo.

## Acknowledgement

I'm extremenly thankful to Processing Foundation for having the faith in me and giving me an opportunity to start the project. There have been several situations where I have been stuck. I express my gratitude to my mentor Saber Khan, other members of Proessing Foundation Cassie Tarakajian, Lauren McCathy, Daniel Shiffman, Cassey Reas for getting back to me and providing me with intelligent advices and suggestions when I contacted them.

I've started this project and doing it with my friend Anupam Asok. I'm so greatful to him for being with me in the development of this project.

I'm so greatful to Andrew Mead and his course in udemy Full Stack Web Development using Meteor https://www.udemy.com/meteor-react/ for it has helped me greatly and Andrew has responded to each and every queries of mine.







