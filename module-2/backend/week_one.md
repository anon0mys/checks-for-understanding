## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  * GET - Requests information without acting on it
  * POST - a request that creates a new record
  * PUT - a request that modifies all of a record
  * PATCH - a request that modifies some of a record
  * DELETE - a request that deletes a record
2. What is Sinatra?
  * Sinatra is a DSL framework built on the Ruby language that allows for easy web based application building.
3. What is MVC?
  * MVC stands for Model View Controller, which is a methodology of web app building that separates functionality into those three roles.
  The controller manages requests and directs traffic from the server to the appropriate model. The model is a database interaction layer that creates an object from the information in the database and passes the requisite information back to the controller. The view is the template that renders the information into an HTML string which is passed back to the controller to be wrapped and returned as a response to a request.
4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  * Conventions are how the Sinatra (and later Rails) DSLs are able to do what is required. The syntax is simplified, but the Sinatra and Rails codebase is written in Ruby, so convention is really more exactly how the Sinatra methods need the arguments in order to run.
5. What types of variables are accessible in our view templates without explicitly passing them?
   * Instance and likely class variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = '1'
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses' do
    erb :index, locals: { name: 'Mr. Ed' }
  end
  ```
9. What's the purpose of ERB?
  * ERB allows us to write Ruby code that will evaluate and pass the values into an HTML template
10. Why do I need a development AND test database?
  * You never want to run tests on a development database, it will pollute the data
11. What is CRUD and why is it important?
  * CRUD stands for Create, Read, Update, and Destroy, which are the four fundamental tasks of a Ruby object that interacts with a database.  
12. What does HTTP stand for?
  * HyperText Transfer Protocol  
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  * <% and <%= are the two opening tags in ERB. The first executes code, the second executes code and interpolates the return value into the HTML string.
14. What's an ORM?
  * Object Relationship Model
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  * ActiveRecord
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  * GET to '/restaurants' lists all of the records in the db
  * GET to '/restaurants/new' allows user to enter new record info
  * POST to '/restaurants' creates a new restaurant record
  * GET to '/restaurants/:id' gets a single restaurant record
  * GET to '/restaurants/:id/edit' allows a user to enter info for an update
  * PUT to  '/restaurants/:id' updates an individual record
  * DELETE to '/restaurants/:id' removes a record from the db
17. What's a migration?
  * A migration is code that modifies the database.
18. When you create a migration, does it automatically modify your database?
  * No, the migration has to actually be run.
19. How does a model relate to a database?
  * The model creates a ruby object or objects from the information in a database row that the rest of the program can then use.
20. What is the difference between `#new` and `#create`?
  * `#new` creates a new Ruby object that we then need to `#save` to the database. `#create` does both.

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?

  ```ruby
    CSV.foreach('films.csv', headers: true, header_converters: symbol) do |line|
      Flim.create(line)
    end
  ```
22. Given the following hash:
  ```ruby
  activities = {
    hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
    karaoke: {cost: $10, supplies: ['courage', 'microphone'],
    brunch: {cost: $35, supplies: ['mimosa flutes'],
    antiquing: {cost: $200, supplies: ['list of antique stores']
  }
  ```
How would I add 'granola bar' to things you should have when hiking?

  ```ruby
    activities[:hiking][:supplies] << 'granola bar'
  ```
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  * SRP- Single responsibility asks that any method or class only be responsible for a single thing
  * Open/Closed- Open/closed means that any code should be able to function independently and allow for the program that holds it to expand without effecting its function, without actually modifying the code.
  * Encapsulation- Means that objects should only know as much as they need to to complete their tasks
  * Dependency Inversion- The things that change most frequently should be dependent on those that change less frequently.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week
