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

### Exercise 2.19 
Suppose that the class Pet has a field called name that is of type String. Write an assignment statement in the body of the following constructor so that the name field will be initialized with the value of the constructor’s parameter.
  Answer:
  private String name;
  public Pet(String petsName)
  {
  	name = petsName;
... }

### Exercise 2.21 
Compare the getBalance method with the getPrice method. What are the differences between them?
Answer: getBalance method returns the value of field balance and getPrice method returns the value of field price.

### Exercise 2.22 
If a call to getPrice can be characterized as ‘What do tickets cost?’, how would you characterize a call to getBalance?
Answer: What is the current balance on the TicketMachine?

### Exercise 2.23 
If the name of getBalance is changed to getAmount, does the return statement in the body of the method need to be changed, too? Try it out within BlueJ.
Answer: No, the getAmount method still returns the balance field value as stated in the method body.

### Exercise 2.24 
Define an accessor method, getTotal, that returns the value of the total field.
Answer:
public int getTotal()
{
  return total;
}

### Exercise 2.25 
Try removing the return statement from the body of getPrice. What error message do you see now when you try compiling the class?
Answer: Error message: "missing return statement". 


### Exercise 2.26 
Compare the method signatures of getPrice and printTicket in Code 2.1. Apart from their names, what is the main difference between them?
Answer: Besides thier names, their return type is the main difference between the getPrice and printTicket methods. getPrice returns price field of return type int but printTicket does not return any value.

### Exercise 2.27 
Do the insertMoney and printTicket methods have return statements? 
Answer: Yes, both have return type of void.
Why do you think this might be? 
Answer: both these methods dont return any value.
Do you notice anything about their headers that might suggest why they do not require return statements?
Answer: The method names are insertMoney and printTickets which suggests it might be performing some operation within the method and void return type is not expected to have any return statement. Also, insertMoney is taking in the parameter of amount which will be used within the method body.

### Exercise 2.28 
Create a ticket machine with a ticket price of your choosing. Before doing anything else, call the getBalance method on it. Now call the insertMoney method (Code 2.6) and give a non-zero positive amount of money as the actual parameter. Now call getBalance again. The two calls to getBalance should show different output because the call to insertMoney had the effect of changing the machine’s state via its balance field.
Answer: Done

### Exercise 2.29 
How can we tell from just its header that setPrice is a method and not a constructor?
public void setPrice(int ticketCost)
Answer: Because setPrice is not the name of the class and also set is a accesser method which typically is not a contructor.

### Exercise 2.30 
Complete the body of the setPrice method so that it assigns the value of its parameter to the price field.
Answer:
public void setPrice(int ticketPrice)
{ 
	price = ticketPrice;
}

### Exercise 2.31 
Complete the body of the following method, whose purpose is to add the value of its parameter to a field named score.
  /**
   * Increase score by the given number of points.
   */
  public void increase(int points)
  {
  	score += points;
... }

### Exercise 2.32 
Can you complete the following method, whose purpose is to sub-tract the value of its parameter from a field named price?
  /**
   * Reduce price by the given amount.
   */
  public void discount(int amount)
  {
    price -= amount;
... }

### Exercise 2.33 
Add a method called prompt to the TicketMachine class. This should have a void return type and take no parameters. The body of the method should print something like:
  Please insert the correct amount of money.
  Answer:
  public void prompt()
    {
        System.out.println("Please insert the correct amount of money.");
    }

### Exercise 2.34 
Add a showPrice method to the TicketMachine class. This should have a void return type and take no parameters. The body of the method should print something like:
The price of a ticket is xyz cents.
where xyz should be replaced by the value held in the price field when the method
is called.
Answer:
public void showPrice()
    {
        System.out.println("The price of a ticket is " + price + "cents");
    }
    
### Exercise 2.35 
Create two ticket machines with differently priced tickets. Do calls to their showPrice methods show the same output, or different? How do you explain this effect?
Answer: 
calls to showPrice methods using two differently priced tickets and two different objects show different output of price. Since i entered different prices for the tickets at the object initialization, the showPrice method returns the price of the object at that instance. 

### Exercise 2.36 
What do you think would be printed if you altered the fourth state- ment of printTicket so that price also has quotes around it, as follows?
  System.out.println("# " + "price" + " cents.");
  Answer:
  The output would just display as price as text and wont return the price field value if price was enclosed in quotes like a  	string.
  
### Exercise 2.37 
What about the following version? 
System.out.println("# price cents.");
Answer:
 The output would still just display as string "# price cents" as text and wont return the price field value.

### Exercise 2.38 
Could either of the previous two versions be used to show the price of tickets in different ticket machines? Explain your answer.
Answer: No, because either of the previous two versions display price as a text/string and does not display the price field value.

### Exercise 2.39 
Modify the constructor of TicketMachine so that it no longer has a parameter. Instead, the price of tickets should be fixed at 1000 cents. What effect does this have when you construct ticket machine objects within BlueJ?
Answer: The price is now initiated with a constant of 1000 cents and does not give a user option to enter the ticket price.

### Exercise 2.40 
Implement a method, empty, that simulates the effect of removing all money from the machine. This method should have a void return type, and its body should simply set the total field to zero. 
Does this method need to take any parameters? 
Answer: No, because we are setting the total to a constant of 0.

Test your method by creating a machine, inserting some money, printing some tickets, checking the total, and then emptying the machine. Is this method a mutator or an accessor?
Answer: This method is a mutator because we have updated/mutated the total field value to a 0.
    public void empty()
    {
        total = 0;
    }

### Exercise 2.41 
Implement a method, setPrice, that is able to set the price of tickets to a new value. The new price is passed in as a parameter value to the method. Test your method by creating a machine, showing the price of tickets, changing the price, and then showing the new price. Is this method a mutator?
Answer: The setPrice method is a mutator.
    public void setprice(int price)
    {
        this.price = price;
    }

### Exercise 2.42 
Give the class two constructors. One should take a single parame- ter that specifies the price, and the other should take no parameter and set the price to be a default value of your choosing. Test your implementation by creating machines via the two different constructors.
Answer:
public TicketMachine(int tkprice)
    {
        this.price = tkprice;
    }
    
   public TicketMachine()
    {
        price = 1000;
        balance = 0;
        total = 0;
    }

