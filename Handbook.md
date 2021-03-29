# Introduction
 
Welcome to your Software Quality Assurance handbook! As an employee at Codeck Software, you are about to gain so much needed knowledge on how we can improve efficiently and code management within your software engineering team. Our goal for this handbook is to help you understand the key elements needed in effective team software programming. The topics we will dive into in this handbook are as follows...

1. Task Estimation in Scrum
2. Coding Standards
3. Code Review

Our goal by the end of you completing this handbook is that you can learn something new about software quality assurance and how to implement it in your future projects at Codeck Software. These core elements will give you the tools to not only improve your projects, but to improve your experience of working within a team at Codeck Software. Thank you and Enjoy!
 
# 1.Task Estimation in Scrum

## Importance of task estimation
- Need to know how long a task is going to take for the team
- Want to deliver efficiently and as fast as possible
- Allows for more up-to-date status reports regarding the sprint
- Resources are shared between tasks, so it is important to know resource dependencies and related time

#### Read more: https://uwaterloo.ca/ist-project-management-office/methodology/project-management/planning/project-schedule/task-estimating

## Common Challenges of Task Estimation

### Idealistic & optimistic estimation
- In most cases, the estimation is carried out under ideal and optimistic conditions, but issues such as unavailability of certain resources, and change requests during the project are not considered in the project estimation.

### Poor design
- A poor design results in unnecessary code tweaking and heavy-duty maintenance applying pressure on schedules.

### Not splitting the tasks enough
- Most projects have a WBS (Work breakdown structure), and each task unit should be equivalent to an Agile story point.
- Lack of this usually implies that there is no proper basis for estimation and then well, it slips out into a subjective guess.

### Ignoring team capacity
- It seems obvious that different people would take different times to code. But when we draw estimates, we come up with a standard effort estimate. This inherently adds a risk layer which is going to make the estimate unreliable.

#### Read more :https://levelup.gitconnected.com/learn-task-estimation-secrets-644e8cbca89e
[![1-1o-Io-JMCGv92-LQNp-Bq-Odz-Qw.png](https://i.postimg.cc/bNcBHCsR/1-1o-Io-JMCGv92-LQNp-Bq-Odz-Qw.png)](https://postimg.cc/bdggqR0G)

### Task estimation techniques

#### Experience
- Draw on previous experience to better predict how many hours will be needed for the sprint
- Can apply to non-developers in equal measure
- Not an exact science but definitely a useful tool for better estimation

#### Ask an expert
- If you have no expertise yourself, it is difficult to accurately determine time for tasks
- There is no shame in asking someone who knows better than you do
- This method can prove to be very efficient

#### Estimation games
- This involves gathering people and putting them into teams
- A bracket format means each team enters their estimation and the closest guess wins
- This method is more involving, light-hearted and can produce great results

### Tips and tricks

#### Create a reasonable buffer
- You always need to give yourself some breathing room to account for setbacks/incidents
- It must be a reasonable time period. Not too long, not too short
- Not the most scientific method but it proves to be very effective

#### Never be afraid to ask
- It is always beneficial to get a different perspective on your work
- Other people will spot problems that you may not even consider

#### Choose the most suitable methods
- Communicating everything through email can be difficult to follow
- I used Jira personally in my internship and found the Kanban board very helpful
- Other examples include Asana, Microsoft Planner

# 2.Coding Standards

### Why use coding standards?
*"Unification decreases development cost standardising development flow and technologies stack"*
[Applying NASA coding standards to javascript](https://www.youtube.com/watch?v=z8hG-3Ak_b4)
- Unification promotes trust, a standardised format of writing code gives confidence that things will work the way they are supposed to.
- In the above video he compares coding standards to aviation development. It takes time to develop a perfect formula so when you do, you should capture it and use it across the board.
- We want our code to be readable, reusable, and easy to maintain for the benefit of all current and future developers.

### Coding Standards to follow at Codeck Software

#### Naming Convention
- Class names should begin with uppercase.
- Variable names should be lowercase.
- Method names should be verbs.
- All method/variable names should be meaningful to their purpose.

#### Files
- All files should use the .java extension.
- Files should be less than 2,000 lines.

#### Commenting and Layout
- Block comments should be used at the beginning of all files to give a description of that file.
- Single and end line comments should be used frequently throughout code to explain functionality of methods and variables.

#### Indentation
- 4 spaces should be used.
- Lines should be no longer than 70 characters.

#### Exception Handling
- Use specific exceptions rather than general.
- Write clear, meaningful error messages.
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
The importance of coding standards needs no explanation. Here's a quick anecdote.
The following quote is taken from What’s Your Worst Experience with a Coding Standard?(https://blog.submain.com/worst-experience-coding-standard/) an article from Erik Dietrich
> Absent a coding standard, you can wind up with a confusing hodgepodge of code. It starts to resemble some medieval map of Europe with fiefdoms and a sprawl of local dialects. “Oh, that’s Dave’s code ? Good luck trying to understand that — Dave LOVES Hungarian notation and is allergic to white space.”
Don't want to be Dave ? Follow our coding standards handbook. You wont regret it!
![Getting Started](https://i.postimg.cc/HLtY6fXS/web-designer-developer-jokes-humour-funny-32.jpg)

### Advantages of using Coding Standards

#### Avoids Risk
- Makes sure the code has no faults
- Results in no software problems
- Reduces the risk of errors

#### Professionalism
- Ensures that a good job is done for the customers or your team
- Your coworkers will be impressed by your level of work, thus resulting in more tasks and more work for you
- As a result of your professional work using the coding standards, new roles may come available to you

#### Time Management
- Good time management will ensure you get the job in time for the customers or your team
- Getting the work done fast but also in an efficient way will boost team morale
- By using the coding standard of commenting, your team will be able to find errors a lot more quickly and fix them
Here is a clear example of effective commenting
```
function addSetEntry(set, value)
{     /*    Don't return `set.add` because it's not chainable in IE 11.  */ 
           set.add(value);    
           return set;  }
```

#### Performance
- When the user is interacting with your code it needs to perform at the fastest and most efficient way possible
- Your application will be extremely slow if coding standards are not met

#### Security
- By the use of coding standards inconsistencies, bugs and errors in logic will be at a minimum
- There is a huge trend in cyber attacks in today's age, so by maintaining a good practice in coding standards, you are protecting Codeck Software

#### Affordability
- Helps to build code that is easy to maintain and perform
- Reusing saves time and lowers development costs
- Can easily set standards in line with the company, increasing flexibility
 
# 3.Code Review
 
## What is Code Review?
Code review is a systematic examination of software source code, intended to hide bugs and to estimate the code quality. It is the act of consciously conveying with fellow programmers to check each other's code for mistakes and review.
 
 
The code review process includes the following stages:
- **Best practice** - Identifying more efficient ways of completing any task.
- **Error detection** - Finding local errors in the code.
- **Vulnerability exposure** - - identifying the most common vulnerabilities in the code.
- **Malware discovery** - A special kind of code review used to detect the suspicious pieces of code or to find the back-doors and any malware integrated into the software.
 
 
## What are the advantages of using code reviews?
 
[An experienced developer's opinion on the advantages of code review](https://simpleprogrammer.com/why-code-reviews-make-better-code-teams/)

#### Reduction of bugs
Code reviews can often catch bugs that testing may not. Particularly when it comes to asynchronous code as the testing environment might have different call back times to the production environment. In this case the tests could miss this bug but a more experienced developer would be more likely to spot it. It is beneficial to have senior developers review juniors' code. The junior developer will write the code to cover the given use cases and then during review it is the job of the senior developer to think of the edge cases and ensure they are handled properly.

#### Code readability
All code you write will have to be maintained and possibly refactored in the future. This may be done by another developer some time in the future so it is important that your code is easy to read and understand. During a code review it will become apparent very quickly if your code is not understandable to another developer so that it can be refactored now rather than a year later with a new developer trying to muddle their way through it when the original author has left the company.

#### Knowledge Sharing
As stated above it is important for senior developers to review the work of juniors as they are more likely to spot bugs. Although juniors are unlikely to spot issues in seniors code there is still value in less experienced developers or new team members performing reviews. A lot can be learned from reviewing and understanding the code of seasoned developers. You will learn the architecture, the prefered style of code, and may even pick up logic that can be reused in the future.
 
 
## Tip To Follow Code Reviews
![Getting Started](https://i.postimg.cc/ncMPgjjb/Overview-of-the-Code-Review-Process.png)
 
#### Developer Side
- Developer designs a piece of code to be reviewed
- It essential to reduce the amount of code you send in a single pull request, therefore, divide up pull request into isolated pieces of logic
- Leave a good description on the, it is very important that the code reviewer recieves context
- Make sure to leave comments addressed to the code reviewer so that they understand designed a certain part of your code which may not be obvious
 
#### Reviewer Side
- When leaving comments on the code you are reviewing you must be as clear and explicit as possible to help the developer
- Establish a process for your team for when to approve or not approve pull requests. It is important that the team understands the coding standards needed
- Reviewers must know when to take something offline rather than keep it in a pull request comment. Rather than going back and forth with the develop, it is better to set up a meeting to discuss this issue as it may take a lot longer via pull request comments
 
## Example
 
Poorly written code is often described as having a “bad smell” that needs to be removed. This is also known as "code hygiene".
 
The following is an example of smelly code:
 
```
public static boolean leap(int y) {
  String tmp = String.valueOf(y);
  if (tmp.charAt(2) == '1' || tmp.charAt(2) == '3' || tmp.charAt(2) == 5 || tmp.charAt(2) == '7' || tmp.charAt(2) == '9') {
      if (tmp.charAt(3)=='2'||tmp.charAt(3)=='6') return true; /*R1*/
      else
          return false; /*R2*/
  }else{
      if (tmp.charAt(2) == '0' && tmp.charAt(3) == '0') {
          return false; /*R3*/
      }
      if (tmp.charAt(3)=='0'||tmp.charAt(3)=='4'||tmp.charAt(3)=='8')return true; /*R4*/
  }
  return false; /*R5*/
}
```
### Use Good Names
 
Good method and variable names are longer and more self-descriptive. Making the code itself more readable can negate the need for comments, with better names that describe the methods and variables.
 
For example, you can rewrite the following line of code
```
int tmp = 86400;  // tmp is the number of seconds in a day (don't do this!)
```
as:
```
int secondsPerDay = 86400;
```
Variable names like tmp, temp, and data are to be avoided. Every local variable is temporary, and every variable is data, so those names are generally meaningless. It is considered much better practise to use a longer, more descriptive name, so that your code reads clearly all by itself. This makes following code easier for both yourself and your fellow programmers and team members.
 
# Conclusions
 
In order to operate an efficient, progressive Sprint team, the three factors that we have written about are all of equal importance. Task estimation is of no benefit without clear coding standards in place with every team member on the same page. Likewise, coding standards are important only if they are being enforced through regular code reviews.
Overall, the most important thing throughout the whole process is to have an open-minded team that has a clear vision of what is required for the task and engage in regular dialogue with each other. This allows for the highest standards and best practices to emerge, leading to a happier, more motivated team and, most importantly, the best possible software for the customer.