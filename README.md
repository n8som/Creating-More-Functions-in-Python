# Creating-More-Functions-in-Python

<h2>Introduction</h2>

Built-in functions are functions that exist within Python and can be called directly. They help analysts efficiently complete tasks. Python also supports user-defined functions. These are functions that analysts write for their specific needs.

For example, patterns in login attempts could reveal suspicious activity. Python functions can help analysts work efficiently with lists of login attempts. Both built-in functions and user-defined functions in Python can help security analysts analyze login attempts.

In this lab, I'll use built-in functions to work with a list of failed login attempts per month to prepare it for further analysis, and I'll define a function that compares the user's login attempts for the current day to their average number of login attempts.

<h2>Scenario</h2>

In my work as a security analyst, I'm responsible for working with a list that contains the number of failed attempts that occurred each month. I'll identify any patterns that might indicate malicious activity. I'm also responsible for defining a function that compares the logins for the current day to an average and improving it by adding a return statement.

<h2>Task 1</h2>

In my work as an analyst, imagine that I'm provided a list of the number of failed login attempts per month, as follows:

119, 101, 99, 91, 92, 105, 108, 85, 88, 90, 264, and 223.

This list is organized in chronological order of months (January, February, March, April, May, June, July, August, September, October, November, and December).

This list is stored in a variable named failed_login_list.

In this task, use a built-in Python function to order the list. I'll pass the call to the function that sorts the list directly into the print() function. This will allow me to display and examine the results.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/4285c389-b1f9-42b2-b8a1-92ea0122b5ae)

The output above shows that the function call to sorted() sorted the failed_login_list in ascending numerical order. The outputted list starts with the lowest number of failed login attempts and ends with the highest number of failed login attempts. The last two numbers in the sorted list (223 and 264) seem to be outlying, indicating an increase in the number of failed login attempts.

<h2>Task 2</h2>

Now, I'll want to isolate the highest number of failed login attempts so I can later investigate information about the month when that highest value occurred.

I'll use the function that returns the largest numeric element from a list. Then, I'll pass this function into the print() function to display the result. This will allow me to determine which month to investigate further.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/fdea5799-1c3f-462b-a270-b43215b9f1f0)

The output above shows that the function call to max() isolated the highest number from the failed_login_list. The highest number of failed login attempts was 264.

<h2>Task 3</h2>

In my work as an analyst, I'll first define a function that displays a message about how many login attempts a user has made that day.

In this task, define a function named analyze_logins() that takes in two parameters, username and current_day_logins. Every time this function is called, it should display a message about the number of login attempts the user has made that day.

Note that the code cell will contain only a function definition, so running it will not produce an output.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/a9737f17-2f85-4048-9bc5-59fb6b4e0fab)

<h2>Task 4</h2>

Now that I've defined the analyze_logins() function, call it to test out how it behaves.

Call analyze_logins() with the arguments "ejones" and 9.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/78e13135-b11e-4a0c-beb9-77be0ebf8cd0)

This function displays the message "Current day login total for ejones is 9" when the arguments are "ejones" and 9. The function is defined in a way that's specific to the user, so it would produce a different output for a different user.

<h2>Task 5</h2>

Now, I'll need to expand this function so that it also provides the average number of login attempts made by the user on that day. Doing this will require incorporating a third parameter into the function definition.

In this task, add a parameter called average_day_logins. The code will use this parameter to display an additional message. The additional message will convey the average login attempts made by the user on that day. Then, call the function with the same first and second arguments as used in Task 4 and a third argument of 3.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/beecbfc8-b4b9-44fa-bc5e-9bef739690a8)

<h2>Task 6</h2>

In this task, I'll further expand the function. Include a calculation to get the ratio of the logins made on the current day to the logins made on an average day. Store this in a new variable named login_ratio. The function displays an additional message that uses this variable.

Note that if average_day_logins is equal to 0, then dividing current_day_logins by average_day_logins will cause an error. Due to the error, Python will display the following message: ZeroDivisionError: division by zero. For this activity, assume that all users will have logged in at least once before. This means that their average_day_logins will be greater than 0, and the function will not involve dividing by zero.

After defining the function, call the function with the same arguments that I used in the previous task.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/04fa0901-c88d-430c-a847-a824300d393b)

This version of the analyze_logins() function displays a user's current day login total, average logins per day, and ratio of current day login total to average logins per day. It produces a distinct output for each distinct username that it takes in.

<h2>Task 7</h2>

I'll continue working with the analyze_logins() function and add a return statement to it. Return statements allow me to send information back to the function call.

In this task, use the return keyword to output the login_ratio from the function, so that it can be used later in my work.

I'll call the function with the same arguments used in the previous task and store the output from the function call in a variable named login_analysis. I'll then use a print() statement to display the saved information.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/be2b32a0-341a-4915-872b-7a3c6eab5ff5)

This version of the analyze_logins() function involves a return statement instead of a print() statement, which allows you to store the output from the function call in a variable for later usage.

<h2>Task 8</h2>

In this task, I'll use the value of login_analysis in a conditional statement. When the value of login_analysis is greater than or equal to 3, then the login activity will require further investigation, and an alert will be displayed. Incorporate this condition to complete the conditional statement in the code.

![image](https://github.com/n8som/Creating-More-Functions-in-Python/assets/110139109/15e4c804-ea2d-437d-9812-1d2dfce9bbe6)

<h2>Conclusion</h2>

What are the key takeaways from this lab?

- There are a variety of ways a function can be written.
  - It can be written to display information to the screen or return information that can then be saved in a variable.
  - Also it can be written to take in any number of parameters, use the parameters to execute a series of tasks, and then return a result.
- The sorted() function in Python is a built-in function that helps me sort the components of a list.
  - For example, when I call sorted() with a list of numbers, it returns the list with the elements in numerical order.
- The max() function in Python is a built-in function that helps me identify the element with the maximum value in a list.
  - For example, when I call max() with a list of numbers, it returns the largest number in the list.
- The print() function in Python is a built-in function that helps display information. It can also be used to directly display the output from another function call.
  - To display the output from another function call, make sure to place it inside a print() statement.

