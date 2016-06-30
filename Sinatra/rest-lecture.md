#### REST and Sinatra Lecture

**Learning Goals**
Students should understand:
+ That REST is a convention for mapping CRUD actions
+ How RESTful actions map to SQL queries
+ How to implement RESTful routes


**Outline**
When we learned methods, learned that we typically ask our methods to do one or more of four things:
+ Reject values
+ Coerce values
+ Act on values
+ Return values

Similarly, all the behavior of a web application (and its representing of our data) can be categorized into five buckets:
  * Create - make a new resources
  * Read - display resources
  * Update/edit - modify a resource
  * Delete - destroy a resource
  * Show - display a single resource

Under the hood, ActiveRecord interprets these instructions into SQL queries:
Select * from books  
Inner join books_genres where  
Where genres.name = 'scary'

RESTful conventions let us map the interactions between our app and our data to a standardized set of URLs.

We refer to a model plus its associated routes and controller as a **resource.**
Twitter -> resource is tweets
Instagram -> resource is picture

For a given resource, we just think of these five actions. If what we're trying to do doesn't fall into one of those five actions, then maybe there is another resource.

We can categorize our entire website into a set of resources and their associated actions, and REST provides the structure.

Examples
Github -> api - interface for accessing data. Should be designed with RESTful conventions in mind:
/users
/users/1
If we follow the convention (and so does the application we want to interact with) we should be able to predict which routes we need to fit to access data.
