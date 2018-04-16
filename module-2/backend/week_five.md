### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
  * Create a div in the application layout html file that prints out flash messages if they exist. Then save desired messages in the session.

2. Where is cart information/temporary information usually stored?
  * In the session

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  * The information in the cart changes regularly and might not need to persist. If you needed to store a user's cart after logout, or to do abandoned cart tracking you would need to save carts.

4. What is the purpose of the asset pipeline?
  * The asset pipeline combines files to reduce the number of requests that are made, speeding up the site.

5. Why do we precompile our assets?
  * Precompiling combines and minimizes all of our javascript and css into a single file.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
  * These are asset pipeline tags that let rails know how to get the assets.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  * A great readme should be well orgnaized, have pre-requisite and setup information, basic how to information. and should be concise and easy to read.

8. What are the top four accessibility issues that we as developers should be aware of?
  * Color blindness, blindness,

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  * It is a callback function. Callbacks live in the model.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
  *  ```ruby scope: ```

11. What is the difference between a scope and a class method?
  * A scope is defined for a subset of the class, where a class method will act on all of the instances of that class.

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?
      * ```ruby session[:cart]['46'] => 4 ```
  12b. How would you increase the quantity of item 29?
      * ```ruby session[:cart]['46'] += 25 ```
  12c. How would you find out how many items your user is thinking about purchasing?   
      * ```ruby session[:cart]values.sum ```

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
  * Polymorphism is the ability of something to have multiple definitions in different places. Several classes can have a hello method that each do different things. Duck-typing is the ability of an object to act like or be treated the same as another object. Activerecord relations behave like arrays, so we can call array methods on them.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  * ```ruby
      clean = string.gsub(/\D/, '')
      clean.insert(3, '.')
      clean.insert(7, '.')
    ```



### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week
