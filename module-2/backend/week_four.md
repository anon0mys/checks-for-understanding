## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  * A small amount of data stored on the client side that gives state to the HTTP cycle
2. What’s the difference between a session and a cookie?
  * A session is stored on the database side and tracks cookies
3. What’s a flash and when do you want to use flashes?
  * A flash is a small amount of information about the current request that is passed to the next request. It is generally used to inform a user about their previous request ie. login success, created a thing, errors
4. Why do people say “HTTP is stateless”?
  * Every request response cycle is independent from the next, and does not remember the previous.
5. What’s authentication? Explain.
  * Authentication is the process of verifying who a user is.
6. What’s the difference between authentication and authorization?
  * Authorization is what the authenticated user is allowed to do.
7. What’s a before filter?
  * A before filter lives in the controller, and performs some kind of authorization check before any action is allowed.
8. How do we keep track of a user once they’ve logged in?
  * Through the session and a cookie. Log in creates a session to track of the user.
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  * Namespacing creates new routes and a new controller for pages that need different access, but does not use a model. Nesting a resource puts the paths to that resource inside the paths to another resource.
10. At a high level, what tools can you use to implement authorization? How would you use them?
  * Sessions and cookies allow for tracking users, enums allow for differentiating the level of access those users have.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  * Enums are a way of tracking the authorization level of a user based on a role attribute.
12. What are some strategies you can use to keep your views DRY?
  * Using partials will help remove duplicate code from multiple views.


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```  
```ruby
holidays = array.reduce([]) do |list, hash|
  list << hash.name
end

print holidays.sort
```
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

```ruby

```


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week
