# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
Answer: ticketMa1
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
Answer: 0

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?
	Answer: Though the ticket price is less than the inserted money and the ticket price, once I call the method printTicket the balance becomes 0.
	* What happens if you insert too much money into the machine – do you receive any refund?
	Answer: No. The too much money just gets added into the total.
	* What happens if you do not insert enough and then try to print a ticket?
	Answer: Calling the printTicket method even without inserting the balance still prints the ticket. Its not checking if there is existing balance before printing the ticket.

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.
	Answer: Done, created multiple objects.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	Answer: created ticketMA2.
	* Does the printed ticket look different?
	Answer: No, the ticketMA2 object ticket and the first object ticketMA1 printed tickets look the same except for the 	difference in the price and balance field values that I entered.

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
	Answer:
	public class Student
	{}
	public class LabClass
	{}

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
	Answer: yes, the class diagram for class TicketMachine has criss cross lines depicting as compile failure.
	* What error message do you get when you now press the compile button?
	Answer: error message on compile time: <identifier> expected.
	* Do you think this message clearly explains what is wrong?
	Answer: message says the class name requires an identifier at the beginning of class wrapper before the keyword 		class.

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
	Answer: Yes, we can leave out the word 'public' from the wrapper of a class.

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
Asnwer: Yes, constructor has the same name as the class and constructor also initiatilizes the instance variables for the first time. Other methods have different names.

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;
Answer: int
private Student representative;
Answer: Student
private Server host;
Answer: Server
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;
Answer: alive
private Person tutor;
Answer: tutor
private Game game;
Answer: game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
Answer: Yes, the order of the three words matter. Field needs to be defined with access modifier followed by data type and then the variable name. The access modifier can be completely removed and just declare as int price which will make the field as public by default.
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
Answer: Yes, the class diagram changes to criss cross lines when there is a compile error.
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
Answer: Yes, Java expects a semicolon at the end of each line to state it as end of statement. So for the field declaration should end with a semicolon.
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.
Answer: private int status;

### Exercise 2.16
* To what class does the following constructor belong?
Answer: Student constructor belongs to Student class.
```
public Student(String name)
```

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
Answer: The Book constructor has 2 parameters and their data types are String and double.
```
public Book(String title, double price)
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
Answer: String bookTitle, int bookYear, string author 
* Can you assume anything about the names of its fields?
Answer: String bookTitle, int bookYear, string author 

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.
