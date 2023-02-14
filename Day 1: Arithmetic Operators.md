Objective

In this challenge, we practice using arithmetic operators. Check out the attached tutorial for resources.

Task

Complete the following functions in the editor below:

getArea(length, width): Calculate and return the area of a rectangle having sides  and .
getPerimeter(length, width): Calculate and return the perimeter of a rectangle having sides  and .
The values returned by these functions are printed to stdout by locked stub code in the editor.

Output Format

image

Sample Input 0

3
4.5
Sample Output 0

13.5
15

## The Solution
```
/**
*   Calculate the area of a rectangle.
*
*   length: The length of the rectangle.
*   width: The width of the rectangle.
*   
*	Return a number denoting the rectangle's area.
**/
function getArea(length, width) {
    // Write your code here
    return length * width;
}

/**
*   Calculate the perimeter of a rectangle.
*	
*	length: The length of the rectangle.
*   width: The width of the rectangle.
*   
*	Return a number denoting the perimeter of a rectangle.
**/
function getPerimeter(length, width) {
    // Write your code here
    return 2*(length+width);
}
```