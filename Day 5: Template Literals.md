Objective

In this challenge, we practice using JavaScript Template Literals. Check the attached tutorial for more details.

Task

The code in the editor has a tagged template literal that passes the area and perimeter of a rectangle to a tag function named sides. Recall that the first argument of a tag function is an array of string literals from the template, and the subsequent values are the template's respective expression values.

Complete the function in the editor so that it does the following:

Finds the initial values of  and  by plugging the area and perimeter values into the formula:
where  is the rectangle's area and  is its perimeter.
Creates an array consisting of  and  and sorts it in ascending order.
Returns the sorted array.
Input Format

The first line contains an integer denoting .
The second line contains an integer denoting .

Constraints

Output Format

Return an array consisting of  and , sorted in ascending order.

Sample Input 0

10
14
Sample Output 0

10
14

## The Solution
```
function sides(literals, ...expressions) {
    let answers = [];
    const A = expressions[0];
    const P = expressions[1];
    const s1 = (P+Math.sqrt(Math.pow(P, 2)-16*A))/4;
    const s2 = (P-Math.sqrt(Math.pow(P, 2)-16*A))/4;
    
    answers.push(s1);
    answers.push(s2);
    
    return answers.sort();
}
```