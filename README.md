# Front End Development Assessment

In this assessment, you'll be implementing a Vue3 application with Typescript and Tailwind. Your task will be to create a dynamic list of beers, fetched from an API, with some specific functionalities. The detailed steps are described below.

## Task Description
Initialize the list
You are provided with a static list of beers. However, in this exercise, we want to make this list dynamic. So, your first task will be to fetch data from an API and display it in your application.

Fetch data from API
To generate the list dynamically, you are required to fetch data from an API. Here is the endpoint you will be working with: https://api.punkapi.com/v2/beers?page=2&per_page=80.

Each entry from this API represents a beer, and you should display the name and first_brewed date in each list item of your Vue application.

## Sorting Functionality
We want to provide users with the ability to sort the list of beers. You should add a functionality to sort the list alphabetically by the name of the beer. You are welcome to use libraries such as lodash or Ramda to help implement this functionality. This means that if a user activates the sorting functionality, the list items should be rearranged so that the beer names are in alphabetical order.

## Add Footer
At the bottom of the page, please add a footer. The footer should be sticky, meaning it should always be visible at the bottom of the viewport regardless of the page length.

In the footer, add a feature that shows the total number of beers fetched from the API. This means that every time the page is loaded or refreshed, the number in the footer should update to reflect the current number of beers in the list.

## Requirements
* Use Vue3 and Typescript for this project.
* Apply Tailwind CSS for the layout and styling.
* Write clean, readable, and maintainable code.
* Upon completion, the application should be a dynamic Vue3 page that fetches and displays a list of beers, allows users to sort the list, and includes a footer that shows the total number of beers. You are welcome to use a library such as lodash or Ramda to achieve the sorting functionality. 

### Good luck!