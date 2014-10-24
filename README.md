<<<<<<< HEAD
Assignment-Intro-to-Git
=======================

The basics of Git usage

## Overview

In this assignment you will demonstrate your ability to use basic Git functionality to clone this repository, make changes to a file on the master branch, make a feature branch, merge the feature branch, roll back a commit.

## Instructions

1. ~~[Fork](https://help.github.com/articles/fork-a-repo) this repository into your GitHub account.~~ Add a file to your your personal team repository in the OSU-CS494-F14 organizaiton (username-Student should be the name of the repo that is auto generated). You should be able to automatially join this organization via [this site hacked together by your instructor](http://idyllic-aspect-573.appspot.com/). Test this early because it is a little held together with [duct tape](http://i.imgur.com/QnZ3XBa.jpg).
  - If you don't want to use GitHub, for this assignment, you may use Git on the Engineering Server but it will be your responsibility to get permissions se up correctly.
2. _Add_ a file called bio.md. This should be a simple, plain text document. If you want to add [fancy formatting](https://help.github.com/articles/markdown-basics) you are welcome to do so.
3. _Commit_ this to your repository that will be turned in.
4. Add some basic  to your bio. Things like hobbies and interests that you want to share.
5. Add a header for a section on _programming background_ (but don't add content).
5. _Commit_ those changes.
6. Make a branch called _programming-bio_.
7. Make at least two commits in this branch adding information about your programming background in the _programming background_ section. This can be things like your favorite project in 161/162 or any other programming work you have done.
8. Switch back to your _master_ branch. 
9. Add more info to your bio and commit that change.
10. Merge the _programming background_ branch with your _master_ branch.
11. Add some more content.
12. _Commit_ that content.
13. Make a _branch_ off the 2nd to last commit called _rewriting-the-future_. Make a change there and commit it.
14. Push all of this to a Git repo the instructor can assess. (Probably your repo in the class organization)

## Final Product

You should have a commit history with the following content:

- Two commits
- A branch off of the 2nd commit called _programming-bio_
  - This branch should have at least 2 commits
- At least one commit after this in _master_
- A commit merging _master_ and _programming-bio_
- At least one commit following that merge
- A branch created after the last commit on master that points to the 2nd to last commit on the master branch. This branch should have 1 commit.

## Grading

The grading will be based on the extent to which the above instructions are followed. If you deviate from the instructions, you will potentially lose points. Even if you think you are 'improving' something.

### Getting an A

This is a bit non-typical as it is not a proper coding assignment. To move from a B to an A, I would suggest doing one or more of the following _on a branch off of the final master commit_. (Everything up to the final _master_ commit should conform to the above requirements)
- Learn to use the GitHub issue system. Open, assign and close an issue.
- Work with someone else. Get some one else to check out and make changes to your repo and you should do the same to their repo.
- Do the same thing again, but use a different version control system and write a short paragraph talking about the differences.
- Intentionally get yourself into a situation that requires merging conflicting work (merging edits to the same lines). Figure out how to correctly merge the content and document the steps you took to do so.
=======
Ajax-Assignment
===============
In this assignment you will do two things. The first is to make a simple Ajax and Local Storage library that can easily be tested the other is to implement a custom weather display page that can remember the users configuration between visits.

General Information
-------------------

Your code should have the following directory structure. You will only put code in the src folder. When we write tests, you will put them in your tests folder. You will have more files than `studentlibrary.js` howevever, that is the file the autmotated tests will run on. It should have the functions from the `Library` section alond with any needed helper functions. All other code for the `Weather` portion also will go in the src directory, but will be put in files your create.

- Repository root
  - Assignment4
    - src
      - studentlibrary.js
    - tests

We will test using gjslint however, the following changes will be made. We will use the `--nojsdoc` flag so you will not get warnings about using JSDoc formatting to document your code (but it is good practice, so feel free to do so if you want to).

Google Style Guide conflicts with JSLint on one point. JSLint wants a space between `function` and `()` when declaring anonymous functions. Google Style Guide does not permit that space. Last week we ignored this difference. For this week there can be no space betwen them. This is correct `function(foo, bar)`. This is not `function (foo, bar)`.

When you are done, the final commit should have the exact commit message 'Assignment 4 final commit.'. We will look for the code assoicated with this commit when grading. The code provided in that commit must exactly match the public hosted code that students will use to test your weather application.

Getting an A
------------
To be eligible to get an A you must complete the tests of 3 other students pages. It will not get you any extra points to do so, but if you do not do so your grade will be capped at a B for the assignment.

Library
-------
The main Ajax function in your library should be a function called `ajaxRequest(URL, Type, Parameters)`. The URL is the base URL that the request will be made to (eg. http://foo.com/page.php). Type will be either the string 'POST' or 'GET' depending on if it is a POST or GET request. Parameters will be an object containing pairs of strings that are key value pairs. So the object literal `{'name':'sally','profession':'doctor'}` would be a valid input parameter `{'doStuff':function (){...}}` would not be legal because a function is not a string. Likewise `{'item':'book','count':50}` would not be legal because 50 is not a string.

This function should return an object of the following format:
```
{
'success': boolean,
'code': string,
'codeDetail': string,
'response': string
}
```
The `success` property should be true if the response had a code corresponding with [success](http://en.wikipedia.org/wiki/List_of_HTTP_status_codes#2xx_Success) and false otherwise. `code` should hold the response code. `codeDetail` should hold the text associated with the particular status code. `response` should be the string representation of the response received from the server.

If the type is a `POST` request the data should be sent as 'application/x-www-form-urlencoded'. This involves setting the content type in the header. An example is given in the Getting Started with Ajax reading on [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/AJAX/Getting_Started#Step_5_.E2.80.93_Working_with_data).

If the type is a `GET` then the proper URL string should be created and used within your function. The key value pairings coming from the URL and Parameter inputs.

The local storage portion of the library will be a simple test to determine if local storage works. This should be a function called `localStorageExists()`. It will return a boolean. If you are able to write and read from local storage, it should return true, otherwise it should return false.

Automated tests will follow later in the week.

Weather
-------
This portion of the assignment is less specific in its requirements. It will use [OpenWeatherMap](http://openweathermap.org/api) as a source of data. Your requirement is to let the user input a city and state as well as select from a number of weather measurements to display. Users can save their settings and when they return they should be automatically loaded. It will be graded using a manual testing protocol by 3 of your classmates. (So that means you will also be manually testing 3 other students sites) Refer to the testing protocol below to see what exact functionality you need.

Weather Testing Protocol
------------------------
- Does the page have a text input for a city name?
- Does the page have a drop down input to select a state?
- Does the drop down have at least the states WA, OR and CA?
- Does the page have the following check boxes?
  - Wind
  - Max Temperature
  - Min Temperature
  - Current temperature
- Does the page have a button labeled 'Save Settings'?
- Does the page have a button labeled 'Get Weather'?
- Input Corvallis into the city text box and select OR from the state drop down.
- Check the wind, current temperature, max temperature and min temperature boxes.
- Click save settings.
- Open a new tab in your browser and navigate back to the page.
- Is the City field populated with Corvallis?
- Is the State field populated with OR?
- Are all the check boxes still checked?
- Uncheck max temperature
- Click 'Save Settings'
- Open a new tab and navigate back to the page
- Are all the settings as before the same except that max temperature is still unchecked?
- Click 'Get Weather'
- Does a list of weather appear on the page containing the following information?
  - City
  - State
  - Current wind direction and speed
  - Minimum temperature
  - Current temperature
- Open (OpenWeatherMap Corvallis)[http://openweathermap.org/city/5720727]
  - Does the weather listed seem to match the information provided on OpenWeatherMap?
- Input 'Seattle' into the city selection.
- Select 'WA' from the drop down.
  - Uncheck everything but wind
- Click 'Get Weather'
  - Has the list been replaced by a new list?
  - Does the new list contain the following?
    - City
    - State
    - Current wind direction and speed
  - Do those values seem to match the values at (OpenWeatherMap Seattle)[http://openweathermap.org/city/5809844]?
>>>>>>> 9bd4d1adc2c0906f6edeb8a6e2e2cbadf2751c0b
