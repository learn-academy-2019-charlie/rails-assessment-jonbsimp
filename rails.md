# Rails Assessments

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

### 1. What are some advantages of using Ruby on Rails?

      -It utilizes model-view-controller (MVC) architecture and is a full-stack framework. With convention over configuration it helps developers to save a lot of time and effort in building applications. 

      -It is very time efficient: Developers do not have to waste time on writing boilerplate code.
      -It is consistent: Developers follow standardized file storage and programming conventions that keep a project structured and readable.
      -It’s cost-effective: uby on Rails is an open source framework distributed under the MIT license, that means you don’t have to spend money on the framework itself. 
      -It provides excellent quality and promotes bug-free development.
      -It’s scalable: f you expect to get a lot of users for your application you should make sure that it can cope with all the visitors you’re hoping to attract. 
      -It’s secure: Some security features are built into the framework and enabled by default. 
      
### 2. How does Ruby on Rails use the Model View Controller (MVC) framework?

    -Models handle the database on the backend, Views are what the user sees (user interface), and the Controllers interact the two together. 

    -The convention ousts configuration, which helps developers to save a lot of their time and effort. 
        Models for handling data and business logic
        Controllers for handling the user interface and application
        Views for handling graphical user interface objects and presentation
    -This separation results in user requests being processed as follows:
        1) The browser (on the client) sends a request for a page to the controller on the server.
        2) The controller retrieves the data it needs from the model in order to respond to the request.
        3) The controller gives the retrieved data to the view.
        4) The view is rendered and sent back to the client for the browser to display.

### 3. Using the information given, complete the steps for creating a new view in a rails app by filling in the blanks:

  1. Create a route: 
  
  code: 
  ```
  get '/about' => 'statics#about' 
  ```
  file: config/routes
  
  2. Create the controller
  
  code: 
  ```
  class StaticsController < ApplicationController
  
  def about 
     render about.html.erb
  end
  ```
  
  file: statics_controller.rb
  
  3. Create the View
  
  code: 
  
  ```
  <div>This is the About page!</div>
  ```
  
  file: about.html.erb
  
  
### 4. Look at these sets of Rails routes, they are an example of which principle/term that we touched on briefly in class? Find the term, and explain why it is important.

```
/users/       method="GET"     # :controller => 'users', :action => 'index'
/users/1      method="GET"     # :controller => 'users', :action => 'show'
/users/new    method="GET"     # :controller => 'users', :action => 'new'
/users/       method="POST"    # :controller => 'users', :action => 'create'
/users/1/edit method="GET"     # :controller => 'users', :action => 'edit'
/users/1      method="PUT"     # :controller => 'users', :action => 'update'
/users/1      method="DELETE"  # :controller => 'users', :action => 'destroy'
```

  These are all CRUD operations.
  
  C-create R-read U-update D-delete
  

### 5. What is the public folder used for in Rails?

  -The public folder is where you will find HTTP error messages.
  -The public directory contains some of the common files for web applications. By default, HTML templates for HTTP errors, such as 404, 422 and 500, are generated along with a favicon and a robots.txt file.

### 6. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

  -get "/game/:guess" => "main#game"

### 7. What are cookies for? How do they work? What is the difference between a session and a cookie?

    -Cookies and Sessions are used to store information. 
    -Cookies are only stored on the client-side machine, while sessions get stored on the client as well as a server.
    -A session creates a file in a temporary directory on the server where registered session variables and their values are stored.

### 8. In an html form, what does the "action" attribute tell you about the form?  How do you designate the HTTP verb for the form?

    -THe action attribute will tell you where the data will be submitted to. The method will be a GET or a POST in all caps to designate the HTTP verb for the form.
    
### 9. Why would you use an instance variable in a rails controller?

    -Use "@"" in your controllers when you want your variable to be available in your views.
    -Using the "@" is an instance variable and is a local variable. Raiils makes instance variables from controllers available to views. 
    -This happens because the template code (erb, haml, etc) is executed within the scope of the current controller instance.
    
### 10. Name two rails generator commands and what files they create:

    1) rails generate model
    2) rails generate controller

### 11. Rails has a great community and lots of free tutorials to help you learn. Here is a list of some tutorials to choose from, choose one, do it, and then report back here at least one thing you learned. You can also use a different resource if you find one that you like better. 

- https://www.tutorialspoint.com/ruby-on-rails/index.htm
- http://railsforzombies.org
- http://guides.rubyonrails.org/getting_started.html
- 
    

    -One thing I found interesting in the tutorialspoint.com ruby on rails guide was Scaffolding.

    -While you're developing Rails applications, especially those which are mainly providing you with a simple interface to data in a database, it can often be useful to use the scaffold method.
    -Scaffolding provides more than cheap demo thrills. Here are some benefits −
        You can quickly get code in front of your users for feedback.
        You are motivated by faster success.
        You can learn how Rails works by looking at the generated code.
        You can use scaffolding as a foundation to jump start your development.


