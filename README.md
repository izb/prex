Prex
====

Prex - The predicate expression parser

Prex gives you a simple predicate expression parser and defines the interface for integration with your application.

It allows you to have a way of expressing decisions based on terms meaningful to your application.

Example
-------

    distance < 20 miles and price in range $5000 to $10000 and colour in {red, black}
    
This expression might be used in an application that deals with a database of cars for sale. The client application might then test a car against the predicate expression and yield a true or false result. In this case it will return true if the car is inside a 20 mile radius of the current location, within the price range of $5-10k and available in either red or black.

It's up to the client application to supply the data; Prex then evaluates the expression and yields the result.

Intended Use Case
-----------------

Prex is most useful where users will wish to be able to filter data based on complex rules. Prex allows them to do this in an expressive manner using a user-friendly grammar.

In low-end situations where users may not wish to go to the effort of writing such expressions for themselves, then prex strings can easily be stored as predefined, easy to maintain filters.

Features
--------

Prex has a wide range of ways of expressing simple values.

Internally, it works only with strings, numbers, booleans and non-nested sets of these three types. Within the language, values can be expressed in a number of real-world ways. E.g. 

- 10000
- 10000.00
- 10,000.00
- 10k
- $10000
- 10 * 1000
- 10 kilometers

are all ways of expressing the number 10,000.



