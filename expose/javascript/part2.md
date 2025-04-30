# Part 1 Answers
## 1. What will happen at line 12 and why? If the code causes an error, explain why.
> '3' would be printed by line 12. This is because variable 'i' is declared in the for loop as var, making it a global variable. Once the for loop ends, 'i' is still declared due to it's a function scope. Since the for-loop had three iterations, 'i' was incremented 3 times from 0. 

## 2. What will happen at line 13 and why? If the code causes an error, explain why.
> '150' would be printed by line 13. Since 'discountedPrice' is a var variable, it becomes a global variable for the function. In the last iteration of for loop, 'discountedPrice' equals prices[2] * (1 - discount), which equals to 300 * (1 - 0.5) = 150. Since 'discountedPrice' is a var, it remains declared when accessing it on line 13. 

## 3. What will happen at line 14 and why? If the code causes an error, explain why.
> '150' would be printed by line 14. The final iteration of the for loop would have 'finalPrice' be Math.round(150 * 100) / 100, which is equal to 15000 / 100 = 150. Since 'finalPrice' is a var variable, it is has function scope capabilities so it still declared even after the for loop ended, allowing line 14 to access 'finalPrice' without errors.

## 4. What will this function return? Give a brief explanation why. If the code causes an error, explain why.
> The function will return a list of the discounted prices that were based on the 'prices' value, which would be [50, 100, 150]. Each iteration of the for loop pushes the 'finalPrice' of that iteration to the 'discounted' list, adding a new value to the list. Each 'finalPrice' would be half of the original due to the 0.5 discount value. 

## 5. What will happen at line 12 and why?  If the code causes an error, explain why. ^^^ (assume this function is being called like the others: discountPrices([100, 200, 300], 0.5)).
> The code causes an error when trying to execute line 12. Since 'i' was declared as a let variable with the execution of the for loop, it is considered within the block scope of the for loop. Anything outside this scope can't access 'i'. When the code executes line 12, it causes an error since the call of the variable is outside the for loop block. It is as if it wasn't declared outside the for loop block. 

## 6. What will happen at line 13 and why? If the code causes an error, explain why.
> The code causes an error when trying to execute line 13. Since 'discountedPrice' is declared within the for loop block, anything outside of it can't access it. With line 13, it is trying to access 'discountedPrice' even though it is outside the block the variable was declared in, making it as if it wasn't declared. 

## 7. What will happen at line 14 and why? If the code causes an error, explain why.
> At line 14, the code would print '150'. Since 'finalPrice' is declared in the same block as line 14, line 14 can access the value of 'finalPrice'. It is 150 because of the last iteration of the for loop changes 'finalPrice', which would be Math.round(150 * 100) / 100 = 150.

## 8. What will this function return? Give a brief explanation. If the code causes an error, explain why.
> The function will return the 'discounted' list, containing the final discounted values of the initial prices, which would be [50, 100, 150]. Each iteration of the for loop pushes the 'finalPrice' of that iteration to the 'discounted' list. Since 'discounted' was declared in the same block as the return statement, the return statement can access 'discounted'. 

## 9. What will happen at line 11 and why? If the code causes an error, explain why.
> The code will cause an error when trying to execute line 11. This is because 'i' is a let variable that is declared in the block of the for loop so nothing outside this block can access 'i'. Because line 11 is trying to access 'i', an error occurs due to line 11 not being in the same block as 'i'.

## 10. What will happen at line 12 and why? If the code causes an error, explain why. 
> When executing line 12, the code will print 3. This would mean that the for loop has successfully executed. Additionally, the 'length' variable stored the length of the inputed 'prices' list (which was 3). Since 'length' is in the same block as line 12, line 12 could access it successfully and print out the value stored in 'length'.

## 11. What will this function return? Give a brief explanation. If the code causes an error, explain why.
> The function wouldn't be able to return due to the code causing an error. Similar to question (9) and (10), the pushing of an element to the const variable 'discounted' would cause it to change, which goes against the const properties. 

## 12. Given the above Object, write the notation for: (These should be in your part2.md)
### A. Accessing the value of the name property in the student object
> student.name
### B. Accessing the value of the Grad Year property in the student object
> student['Grad Year']
### C. Calling the function for the greeting property in the student object
> student.greeting()
### D. Accessing the name property of the object in the Favorite Teacher property in student
> student['Favorite Teacher'].name
### E. Access index zero in the array of the courseLoad property of the student object
> student.courseLoad[0]

## 13. Arithmetic
### A. '3' + 2
> '32'
### B. '3' - 2
> 1
### C. 3 + null
> 3
### D. '3' + null
> '3null'
### E. true + 3
> 4
### F. false + null
> 0
### G. '3' + undefined
> '3undefined'
### H. '3' - undefined
> NaN

## 14. Comparison
### A. '2' > 1
>true
### B. '2' < '12'
>false
### C. 2 == '2'
>true
### D. 2 === '2'
>false
### E. true == 2
>false
### F. true === Boolean(2)
>true

## 15. Explain the difference between the == and === operators.
> The difference betwene the == and === operations is that == is an equality operator that checks if two things are equal while considering type conversion. For example, 2 == '2' is true because with type conversion, '2' is 2 when transformed from a string to a number. On the other hand, === is an equality operator that checks if two things are equal without type conversion. Using the same example, even though '2' can be converted into 2, 2 is not the same as '2' without type conversion because 2 is a number and '2' is a string, so 2 === '2' is false. Simply, == checks if two things are equal regardless of the type, but === checks if two things are equal and are the same type. 

## 17. If the function above is called with the following parameters modifyArray([1,2,3], doSomething), what will be the result? Briefly walk through how you arrived at that result.
> The result would be a new array that is double the value of the original so the new array would be [2,4,6]. The **modifyArray([1,2,3], doSomething)** has array be [1,2,3] and callback be doSomething (which is a function). newArr is created, which will be returned at the end of the modifyArray function. For each iteration of the for loop, a new value will be pushed onto the newArr. This value is determined through a function call. Since callback is doSomething, the value that is pushed onto the newArr is the value that is returned from calling of the doSomething function with the parameter as the ith element of the original array. The doSomething function returns double of the input number. After the for loop is done executing and pushing double the number for each value in the original array, newArr will return and would have double of each element in the original array. The returning array would be [2,4,6]. 

## 19. What is the output of the above code?
> The output of the code would be 1, 4, 3, 2. This is because the printing of 1 and 4 doesn't have any delays. 3 is next but is after 4 because even though the delay is 0, there is still some delay (it is just very small). 2 is next because the delay is the longest.