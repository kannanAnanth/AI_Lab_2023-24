# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
likes(john, food).
food(apples).
food(chicken).
eats(sue, X) :- eats(bill, X).
eats(bill, peanuts).
likes(john, X) :- food(X).
likes(john, X) :- eats(bill, X).
?- likes(john, apples).
```

### Output:
![image](https://github.com/Chandru0021/AI_Lab_2023-24/assets/131637082/1277a537-1433-4179-92ab-54c657de39e0)

### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve,X):-
     easycourse(X).
hard(sciencecourse).
easycourse(X):-
          course(X,dept(havefun)).
course(bk301,dept(havefun)).
```
### Output:
![image](https://github.com/Chandru0021/AI_Lab_2023-24/assets/131637082/7ff2db61-a2d5-4b6b-a70e-adac9e89f4f6)

### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
american(colonel_west).
enemy(nano).
owns(nano, missiles).
sells(colonel_west, weapons) :- american(colonel_west).
criminal(X) :- sells(X, weapons), owns(Y, missiles), enemy(Y).
?- criminal(colonel_west).

```
### Output:
![image](https://github.com/Chandru0021/AI_Lab_2023-24/assets/131637082/4d5467d8-f648-4bd1-9460-9b4bf9977d72)

### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
