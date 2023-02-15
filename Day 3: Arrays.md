Objective

In this challenge, we learn about Arrays. Check out the attached tutorial for more details.

Function Description

Complete the getSecondLargest function in the editor below.

getSecondLargest has the following parameters:

int nums[n]: an array of integers
Returns

int: the second largest number in 
Input Format

The first line contains an integer, , the size of the  array.
The second line contains  space-separated numbers that describe the elements in .

Constraints

, where  is the number at index .
The numbers in  may not be distinct.
Sample Input 0

5
2 3 6 6 5
Sample Output 0

5

## The Soultion
```
function getSecondLargest(nums) {
    // Complete the function
    let first = nums[0];
    let second = nums[0];
    for(let i of nums){
       if(i > first){
           second = first;
           first = i;
       }
       if(i > second && i < first){
           second = i
       }
    }
    return second;
}
```