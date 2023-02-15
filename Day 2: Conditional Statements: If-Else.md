Objective

In this challenge, we learn about if-else statements. Check out the attached tutorial for more details.

Task

Complete the getGrade(score) function in the editor. It has one parameter: an integer, , denoting the number of points Julia earned on an exam. It must return the letter corresponding to her  according to the following rules:

If , then .
If , then .
If , then .
If , then .
If , then .
If , then .
Input Format

Stub code in the editor reads a single integer denoting  from stdin and passes it to the function.

Constraints

Output Format

The function must return the value of  (i.e., the letter grade) that Julia earned on the exam.

Sample Input 0

11
Sample Output 0

D

## The Solution
```
function getGrade(score) {
    let grade =
    score <= 5
      ? 'F'
      : score <= 10
      ? 'E'
      : score <= 15
      ? 'D'
      : score <= 20
      ? 'C'
      : score <= 25
      ? 'B'
      : score <= 30
      ? 'A'
      : '';
    // Write your code here

    return grade;
}
```