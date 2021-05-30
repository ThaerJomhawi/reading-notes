# **Loops**
***loops*** offer a quick and easy way to do something repeatedly.

You can think of a ***loop*** as a computerized version of the game where you tell someone to take X steps in one direction, then Y steps in another

There are many different kinds of ***loops***, but they all essentially do the same thing: they repeat an action some number of times. (Note that it's possible that number could be zero!)

The various ***loop*** mechanisms offer different ways to determine the start and end points of the loop. There are various situations that are more easily served by one type of loop over the others.

# ***for statement***
A *for-loop* repeats until a specified condition evaluates to false.

When a *for-loop* executes, the following occurs:

The initializing expression **initial Expression **, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.

The conditionExpression expression is evaluated. If the value of conditionExpression is true, the loop statements execute. If the value of condition is false, the for loop terminates.

The statement executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.

If present, the update expression incrementExpression is executed.

Control returns to Step 2.*


![JS](https://www.tutorialspoint.com/javascript/images/for_loop.jpg)

# ***while statement***
A while statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:

while (condition) statement

If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.

The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.

To execute multiple statements, use a block statement ({ ... }) to group those statements.

![JS](https://www.north-47.com/wp-content/uploads/2020/06/1_JA57AArvHLn3tulDxJKzEg.jpeg)