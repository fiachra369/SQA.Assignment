# Code Review

## What is code Review?
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

In conclusion, Coding review is an extremely important aspect in software engineering. This is clearly highlighted in this article by Erik Dietrich , Code Review Horror Stories(https://blog.submain.com/code-review-horror-stories/). He talks about how, at the end of the day, coding reviews need to used not as a for of criticism but as a way to improve and benefit the company

> "Code review is far too valuable to eliminate, so you need to learn to optimize it for effectiveness and sanity. ?But you need to understand that it’s a highly
> collaborative activity that inherently involves criticism and contradictory ideas. ?If you have underlying personnel problems in your group, code review will
> bring them out in spades".