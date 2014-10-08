Assignment-HTML-CSS-Forms
=========================
In this assignment you will make a simple HTML page, styled with CSS that has a pair of forms, one which submits via a POST and one which submits via a GET.

**This assignment is subject to minor revision in order to facilitate easier testing. Check back after Thursday at 11:59pm to check for any changes to the assignment. The changes may involve things like changing the URL the form points to or adding specific ids to certain elements so that the tester can find those elements. They will not be major changes.**

##Instructions
- Make a new folder called 'assignment2' in your class repository.
- Make a layout.html and style.css file in that directory.
  - These files will be the only files used for grading this assignment.
  - If they are not named properly they will not get graded by the script.
  - All styling should be applied from style.css.
  - No ids should be used except where specified in the assignment.
- If you wish to do extra work (for example, to move to an A) make a subdirectory within 'assignment2' called 'extra'
  - The main page in that directory should be called index.html.
- This assignment must be hosted on a live web server. When you submit you will need to include a URL to the live version of the page.

##Requirements
- Create a table that has that is 6x6 (inclusive of the header row and header cells).
  - The upper left cell should be empty. The others shoudl be non-empty.
  - The table should have a caption detailing the contents of the table.
  - The table should have a header section, all the cells in this section should have bold text. (This is the default for th)
  - The first column of the table should have header cells that have italic text. (These should not be bold)
  - The first non-header cell of each non-header row should have 'red' text
  - The third non-header cell of each non-header row should have 'blue' text
  - The table should have a footer section made up of two cells, one should be one column wide, the other should be 4 columns wide.

- Create a dl list with at least 3 entries
  - When you hover over a dt entry, its dd item should get a 'purple' background
 
####Sample Table and List
![Table and List Example](http://i.imgur.com/VlNphtT.png)

- Create two forms. One should submit via a post, the other via a get, they should have identical content.
  - There should be 4 input types
    - A text input with a name attribute of 'text_input'
    - A number input with a name attribute of 'numerical_input'
    - A password input with a name attribute of 'password_input'
    - A set of radio inputs
      - They should be named 'candy'
      - These options should exist in this order
        - Snickers
        - Skittles
        - Mentos

####Sample From
![Form Example](http://i.imgur.com/JL9q3Bf.png)  

- Create the following div layout. Give the divs ids of 'red', 'orange', 'yellow', 'green', 'blue', 'indigo' in reading order (left to right, top to bottom, like they are colored in the picture) also apply those colors for their respective backgrounds.
  - For the first two rows of divs only use top and left margins to control placement. You can use width and height to control size and then you may need to use clear and float in order to get positioning right.
  - For the last row set all the horizontal spacing using only left and right margins on the right div.

####Div Measurements
![Div Layout](http://i.imgur.com/NjlPQK2.jpg)

####Sample Divs
![Live Div Example](http://i.imgur.com/bYgy8Fc.png)
