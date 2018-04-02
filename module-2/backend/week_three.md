## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  * rails new App (you can include -T, -d, or --skip-'gem' to modify how you want the app to be built.)
2. What do Models generally inherit from in rails?
  * ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
  * ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  * resources :horse, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
  * 'rails routes' gives you the route helper, HTTP verb, actual path, and the controller and action that are associated.
6. What is an example of a route helper? When would you use them?
  * route helpers are shorthand for the full route, like: 'new_horse_path'
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  * Path is relative while url is absolute. Meaning, `_url` will give the full url while path will give just the uri.
8. What are strong params and why are they necessary?
  * Strong params are a private model method that explicitly states which params are required and which are permitted for use in the model.
9. What role does `form_for` play in helping us create our forms?
  * `form_for` creates a form based on the object that it is passed, and will automatically title buttons and use appropriate Verbs based on what it is doing, either creating or updating an object.
10. How does `form_for` know where to submit the user's input?
  * It will use the object it is passed.
11. Create a form using a `form_for` helper to create a new `Horse`.
 ```
  <%= form_for Horse.new do |horse| %>
    <%= f.label :name %>
    <%= f.text_field :name %>

    <%= f.submit %>
  <% end %>
  ```
12. Why do we want to validate our models?
  * To make sure that when a user inputs information they cannot create a record without putting something in all of the appropriate fields.
13. What are the steps of the DNS lookup?
  * First the browser requests a DNS lookup on the computer's dns library to convert a domain name into an IP address. If there is no record the computer will ask the router, then the ISP, then the ISP's provider, then to the DNS root servers.


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?

```ruby
  def move
    prance
  end
```

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?

```ruby
  furniture[:table][:height]
  => 3
  furniture[:purchased]
  => true
```

16. What is inheritance?
  * Inheritance allows a class to make use of all of the inherited class' methods and states. If Supermutt inherits from dog, and dog has an instance variable fur and a method bark, Supermutt will have both a fur variable and a bark method available.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week
