# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE:23.09.2023                                                                           
### REGISTER NUMBER : 212221040022
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

likes(john,X):- 
	food(X). 
	eats(bill,X):- 
	eats(sue,X). 
	eats(Y,X):- 
	food(X). 
	eats(bill,peanuts). 
	food(apple). 
	food(chicken). 
	food(peanuts).

### Output:
<img width="454" alt="Screenshot 2023-11-07 220948" src="https://github.com/21005291/AI_Lab_2023-24/assets/112933167/439b0fbd-0e83-4c6d-8a64-8a653d391828">


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
	likes(steve,X):- 
	easycourse(X). 
	hard(sciencecourse). 
	easycourse(X):- 
	course(X,dept(havefun)). 
	course(bk301,dept(havefun)).





### Output:
<img width="451" alt="Screenshot 2023-11-07 221055" src="https://github.com/21005291/AI_Lab_2023-24/assets/112933167/fd474c35-4747-4bea-964f-e9e966df66c3">

### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
criminal(X):- 
	american(X), 
	weapon(Y), 
	hostile(Z), 
	sells(X,Y,Z). 
	weapon(Y):- 
	missile(Y). 
	hostile(Z):- 
	enemy(Z,X). 
	sells(west,Y,nano):- 
	missile(Y), 
	owns(nano,Y). 
	missile(m). 
	owns(nano,m). 
	enemy(nano,america). 
	american(west).



### Output:
<img width="454" alt="Screenshot 2023-11-07 221117" src="https://github.com/21005291/AI_Lab_2023-24/assets/112933167/2a58728e-294f-4a19-8290-c7b32eb0623b">

### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
