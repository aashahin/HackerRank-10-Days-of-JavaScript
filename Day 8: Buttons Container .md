Objective

In this challenge, we lay out buttons inside a div and modify their labels after each click event on one of the buttons. Check out the attached tutorial for learning materials.

Task
We want to create nine buttons enclosed in a div, laid out so they form a  grid. Each button has a distinct label from  to , and the labels on the outer buttons must rotate in the clockwise direction each time we click the middle button.

Complete the code in the editor so that it satisfies the following criteria:

Initial State. The initial layout looks like this:
layout
Element IDs. Each element in the document must have an id, specified below:

The button container div's id must be btns.
The initial innerHTML labels must have the following button ids:
innerHTML	id
1	btn1
2	btn2
3	btn3
4	btn4
5	btn5
6	btn6
7	btn7
8	btn8
9	btn9
Styling. The document's elements must have the following styles:
The width of btns is , relative to the document body's width.
Each button (i.e., btn1 through btn9) satisfies the following:
The width is , relative to its container width.
The height is 48px.
The font-size is 24px.
Behavior. Each time btn5 is clicked, the innerHTML text on the grid's outer buttons (i.e., bt1, btn2, btn3, btn4, btn6, btn7, btn8, btn9) must rotate in the clockwise direction. Do not update the button id's.
The .js and .css files are in different directories, so use the link tag to provide the CSS file path and the script tag to provide the JS file path:
```
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="css/buttonsGrid.css" type="text/css">
    </head>
    
    <body>
    	<script src="js/buttonsGrid.js" type="text/javascript"></script>
    </body>
</html>
```

## The Solution
- Javascript
```
  window.onload = () => {
  const button5 = document.getElementById('btn5');
  button5.addEventListener('click', () => {
    let arr = [
      document.getElementById('btn1').innerText,
      document.getElementById('btn2').innerText,
      document.getElementById('btn3').innerText,
      document.getElementById('btn6').innerText,
      document.getElementById('btn9').innerText,
      document.getElementById('btn8').innerText,
      document.getElementById('btn7').innerText,
      document.getElementById('btn4').innerText
    ];
    arr = [...arr.slice(arr.length - 1), ...arr.slice(0, arr.length - 1)];
    document.getElementById('btn1').innerText = arr[0];
    document.getElementById('btn2').innerText = arr[1];
    document.getElementById('btn3').innerText = arr[2];
    document.getElementById('btn6').innerText = arr[3];
    document.getElementById('btn9').innerText = arr[4];
    document.getElementById('btn8').innerText = arr[5];
    document.getElementById('btn7').innerText = arr[6];
    document.getElementById('btn4').innerText = arr[7];
  });
};
```
- Css
```
#btns {
  display: block;
  overflow: hidden;
  width: 75%;
}
#btns button {
  display: block;
  width: 30%;
  float: left;
  height: 48px;
  font-size: 24px;
}
```
- HTML
```
<!-- Enter your HTML code here -->
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Buttons Grid</title>
        <link rel="stylesheet" href="css/buttonsGrid.css" type="text/css" />
    </head>
    <body>
      <div id="btns">
      <button id="btn1">1</button> <button id="btn2">2</button>
      <button id="btn3">3</button> <button id="btn4">4</button>
      <button id="btn5">5</button> <button id="btn6">6</button>
      <button id="btn7">7</button> <button id="btn8">8</button>
      <button id="btn9">9</button>
    </div>
    <script src="js/buttonsGrid.js" type="text/javascript"></script>
    </body>
</html>
```