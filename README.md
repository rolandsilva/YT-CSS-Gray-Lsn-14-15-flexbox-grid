# YT-CSS-Gray-Lsn-14-15-flexbox-grid

YT CSS Gray Lsn 14-15 flexbox/grid

/_ YT CSS Gray Lesson 15 Grid CSS _/

@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

- {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }

body {
font-family: "Roboto", sans-serif;
min-height: 100vh;

    display: grid;
    grid-template-columns: repeat(9, 1fr);
    grid-auto-rows: 50px auto 50px;
    grid-template-areas:
        "hd hd hd hd hd hd hd hd hd"
        "mn mn mn mn mn mn mn sb sb"
        "ft ft ft ft ft ft ft ft ft";
    column-gap: 0.5rem;
    /* gap: 0.5rem; */

}

.el {
background-color: rebeccapurple;
color: white;
display: grid;
place-content: center;
}

.header {
grid-area: hd;
}

.sidebar {
grid-area: sb;
background-color: blue;
}

.footer {
grid-area: ft;
}

.container {
display: grid;
grid-area: mn;
height: 400px;
/_ height: 800px; _/
/_ (for template-rows and auto-columns) _/

    /* •	Controls the flow of grid items when they are placed automatically (without explicitly specifying their position). It defines whether they are placed by row or column. */
    /* grid-auto-flow: column; */

    /* grid-template-columns/rows	Defines the number and size of columns or rows in the grid. You can specify them in any valid CSS unit (e.g., pixels, percentages, fractions). */
    /* grid-template-columns can be mixed units */

    /* grid-template-columns: 200px 100px 200px; */

    /* grid-template-columns with units, 3 columns */
    /* /* grid-template-columns: 2fr 1fr 1fr; */
    /* grid-template-columns: 200px 1fr 1fr; */

    /* grid-template-columns with repeat, 4 columns in a row,   has to be a pattern*/
    /* grid-template-columns: repeat(4, 1fr); */


    /* 2 columns (* 6 div items (3 pairs)) wraps into two rows */
    /* grid-auto-rows/columns auto grows row with min 150px up to as much as the height of the container (in this case 400px height) */
    grid-template-columns: repeat(2, 1fr 2fr);
    grid-auto-rows: minmax(150px, auto);

    /* also can have the opposite */
    /* grid-template-rows: repeat(2, 1fr 2fr);
    grid-auto-columns: 150px; */
    /* grid-auto-columns: minmax(150px, auto); */

    /* 4 columns in a row,   has to be a pattern*/
    /* grid-template-columns: repeat(4, 1fr); */

    /* column/row gaps  shorthand */
    /* gap: 1rem 0.5rem; */
    gap: 1rem;
    /* row-gap: 10px;
    column-gap: 20px; */

}

.box {
background-color: #000;
color: #fff;
font-size: 2rem;
padding: 0.5rem;
}

.box:first-child {
background-color: blue;

    /* Individual properties */
    /* grid-column-start: 1;
    grid-column-end: 4;
    grid-row-start: 1;
    grid-row-end: 3; */

    /* Shorthand for grid-column and grid-row */
    grid-column: 1 / 4;
    grid-row: 1 / 3;

    display: grid;
    /* align-content: center;
    justify-content: center; */

    /* shorthand for align-content and justify-content */
    /* place-content: center center; */
    place-content: center;

}

.box:nth-child(2) {
background-color: purple;
grid-column: 1 / 5;
grid-row: 3 / 4;
}
