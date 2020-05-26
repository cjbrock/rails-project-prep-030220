# Rails Project Prep!

## Project Requirements

### Use the Ruby on Rails framework

### Your models must include at least one has_many, at least one belongs_to, and at least two has_many :through relationships

  User
  has_many user_todos
  has_many todos, though user_todos

  User_todos
  belong_to user
  belong_to todo

  Todo
  has_many user_todos
  has_many users, though user_todos

### The join table must include a user-submittable attribute

  - due date on our UserTodo table

### Your models must include reasonable validations for the simple attributes

  - validates :username, presence: true, uniqueness: true
  - Bcrypt automatically validates presence of password

### Your forms should correctly display errors within a fields_with_errors class, and be visible within the view

- to get the field_with_errors div, make sure you are using form_with

### You must include at least one class level ActiveRecord scope method

- scope methods return a subset of your data
- scope methods NEED TO BE CHAINABLE

scope :completed_todos, -> { where(complete: true)} 

same as this:

 def self.completed_todos
    where(complete:true)
  end


### Your application must provide standard user authentication, including signup, login, logout, and passwords

- Can use either Devise or native authentication
- make sure that you can explain either way

### Your authentication system must also allow login from some other service. Facebook, Twitter, Foursquare, Github, etc...

- usually through Omniauth
- the easiest ones are usually Github, sometimes Facebook or Google

### You need full CRUD functionality for one model

### You must include either a nested index or show route

### You must include a nested new route



### Project notes

- It should be as DRY as possible
- If you scaffold it, you will probably automatically fail. It generally means that you don't know what your code is doing, because you took so many shortcuts to get there. Once you know what your code is doing, then shortcuts are ok. I'll show you how to effectively scaffold stuff next section.
- Make sure you're committing early and often. You want more than 50 commits here - they'll look at your github repo and you'll be graded on it.
- You also want a GOOD README. A good README has 4 parts: An application description, an installation guide, a contributor's guide (how someone would go about adding to the app if they want to), and a licensing statement. Even if you have a licensing file, you still need a statement that says "This project is licensed under the MIT Open Source Public License." or whatever you choose to use.

## Corinna builds (most of) an application

 - I believe this is only missing Omniauth. Bryant built Omniauth with Devise last week. We can do Omniauth with Native Rails next week.
 
[Part 1 Video](https://youtu.be/N48aA2YFIos)
[Part 2 Video](https://youtu.be/2Ozo4lcEuho)
[Code](https://github.com/cjbrock/bourbon-baller)