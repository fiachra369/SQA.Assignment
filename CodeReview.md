## What is code Review ? - Victor
Code review is a systematic examination of software source code, intended to bugs and to estimate the code quality. It is the act of consciously conveying with fellow programmers to check each other's code for mistakes and review.


The code review process includes the following stages:
- **Best practice** - Identifying more efficient ways of completing any task. 
- **Error detection** - Finding local errors in the code.
- **Vulnerability exposure** - - identifying the most common vulnerabilities in the code.
- **Malware discovery** - A special kind of code review used to detect the suspicious pieces of code or to find the back-doors and any malware integrated into the software.







## What are the advantages of using code reviews ? - Siobhan

## Tip To Follow Code Reviews
![Getting Started](https://i.postimg.cc/ncMPgjjb/Overview-of-the-Code-Review-Process.png)

#### Developer Side
- Developer designs a piece of code to be reviewed
- It essential to reduce the amount of code you send in a single pull request, therefore, divide up pull request into isolated pieces of logic
- Leave a good description on the, it is very important that the code reviewer recieves context
- Make sure to leave comments addressed to the code reveiwer so that they understand designed a certain part of your code which may not be obvious

#### Reviewer Side
- When leaving comments on the code you are reviewing you must be as clear and explicit as possible to help the developer 
- Establish a process for your team for when to approve or not approve pull requests. It is important that the team understands the coding standards needed
- Reviewers must know when to take something offline rather than keep it in a pull request comment. Rather than going back and forth with the develop, it is better to set up a meeting to dicuss this issue as it may take a lot longer via pull request comments

## Anecdote & Example 

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
Variable names like tmp, temp, and data are to be avoided. Every local variable is temporary, and every variable is data, so those names are generally meaningless. It id considered much better practise to use a longer, more descriptive name, so that your code reads clearly all by itself. This makes following code easier for both yourself and your fellow programmers and team members.



