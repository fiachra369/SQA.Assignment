# Coding Standards

### Why use coding standards?

*"Unification decreases devlopment cost standardizing development flow and technologies stack"*

Applying NASA coding standards to javascript: https://www.youtube.com/watch?v=z8hG-3Ak_b4

- Unification promotes trust, a standardised format of writing code gives confidence that things will work the way they are supposed to.
- In the above video he compares coding standards to aviation development. It takes time to develop a perfect formula so when you do, you should capture it and use it across the board. 
- We want our code to be readable, reusable, and easy to maintain for the benefit of all current and future developers.

### Coding Standards to follow at Codeck Software

#### Naming Convention
- Class names should begin with uppercase.
- Variable names should be lowercase.
- Methods names should be verbs.
- All method/variable names should be meaningful to their purpose.


#### Files  
- All files should use .java extension.

#### Commenting and Layout  
- Block comments should be used at the beginning of all files to give a description of that file.
- Single and end line comments should be used frequently throughout code to explain functionality of methods and variables.


#### Indention  


#### Exception Handling  


**Difficult to read and understand:**  

```
    private int a = 100;
	private int b = 20;
	
	public int withdraw(int b) {
	a = a-b;
	return a;
	}
```


**Easy to read and understand:**  

```
    private int accountBalance = 100; //current account balance
	private int withdrawalAmount = 20; //amount to withdraw
	
	//method to calculate new account balance after withdrawal
	public int withdraw(int withdrawalAmount) {
		accountBalance = accountBalance - withdrawalAmount;
		return accountBalance;
	}
```

The importance of coding standards needs no explanation. Heres a quick anecdote.

The following quotes is taken from What’s Your Worst Experience with a Coding Standard?(https://blog.submain.com/worst-experience-coding-standard/) an artical from Erik Dietrich

> Absent a coding standard, you can wind up with a confusing hodgepodge of code.? It starts to resemble some medieval map of > Europe with fiefdoms and a sprawl of local dialects.? “Oh, that’s Dave’s code.? ?Good luck trying to understand that — Dave > LOVES Hungarian notation and is allergic to white space.”

Dont want to be Dave ? Follow our coding standards handbook. You wont regret it!

### Advantages of using Coding Standards

####Avoids Risk
- Makes sure the code has no faults
- Results in no software problems 
- Reduces the risk of errors 

####Professionalism
- Ensures that a good job is done for the customers or your team
- Your coworkers will be impressed by your level work, thus resulting in more tasks and work for you
- As a result of your professional work using the coding standards new roles may come available to you


####Time Management
- Good timemanagement will ensure you get the job in time for the customers or your team
- Getting the work done fast but also in an efficient way will boost team moral 
- By using the coding standard of commenting, your team will be able to find errors a lot more quickly and fix them

Here is a clear example of affective commenting

```
function addSetEntry(set, value) 
{     /*    Don't return `set.add` because it's not chainable in IE 11.  */   
             set.add(value);      
			 return set;  }
``


####Performance 
- When the user is interacting with your code it needs to perform at the fastest and most efficient way possible
- Your application will be extremely slow if coding standards are not met

####Security
- By the use of coding standards inconsistencies, bugs and errors in logic will be at a minimum
- There is a huge trend in cycber attacks in todays age, so by maintaining a good practice in coding standards, you are protecting Codeck Software


