# CRUD Quiz

Use the solution to this afternoon's Property Tracker lab to answer the following questions. Please write your answers under each question, push the file to GitHub, and submit in the usual way.

## MVP Questions

In our Property Tracker application:

Q1. Where are we instantiating instances of the `Property` class?
property.rb
Q2. Where are we defining the SQL that enables us to save the ruby `Property` object into the database?
properties.sql
Q3. In `console.rb`, which lines modify the database?
13, 22, 31, 33
Q4. Why do we not define the id of a `Property` object at the point we instantiate it (‘new it up’)?
The database defines the id for us
Q5. Where and how do we assign the id (that is generated by the database) to the ruby `Property` object?
in property.rb line 32 we assign the id by returning it from the database
Q6. Why do we put a guard (an `if` clause) on the `@id` attribute in the constructor?
if the id doesn't exist it will return nil instead of returning 0
Q7. Why are some of the CRUD actions represented by instance methods, and others by class methods?

Q8. What type of data structure is returned by calls to `db.exec_prepared()`? In the `save` method, how do we access the id from the returned data structure?
its an array, we access it by location [0][id] then change it to an integer
Q9. Why do we use prepared statements when performing database operations?
we can use them multiple times
## Extension Questions

Look at the `find_by_id` and `find_by_address` methods in the `Property` class.

Q10. What do they take in as their arguments?
they take in thhe columns id and address as arguments
Q11. What are their return values?
they return the relevant sql table row
