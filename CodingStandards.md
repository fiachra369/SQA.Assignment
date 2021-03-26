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

### Advantages of using Coding Standards

