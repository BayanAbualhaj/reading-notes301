# What I learned 


![ejs](https://miro.medium.com/max/875/1*XP-mZOrIqX7OsFInN2ngRQ.png)


## Watch EJS tutorial 

1. Getting Started:
    - create an instance for the server     
        * install : express , path , core and body-parser 
        * the app.use express and core 
        * set the views and views ingine 
        * set the route and the handler (call back function)

2. Inject values inside the views :
    - response.render take 3 parameters 
        * the name if the file (index.ejs) with out the path 
        * an object or an array to pass to the view 
    
    - every ejs syntax has an opening and closing tag <% %> for the statements and <%= %> to set a value in them and to destroy smth just add / before and after the opening and the closing tag

3. for loop and arrays 
    - we can pass an array of object or an array of arrays 
    - we can render by ejs any thing we want 
        * example ('index',people[
            {name:'Jerry'},
            {name:'dave'}
        ])
    -and we can pass them to the view by a foor loop 

4. if/else 
    - as well as the for loop we can put the if statement in side it for any condition.



## How To Use EJS to Template Your Node Application 


* Jade comes as the view engine for Express by default but Jade syntax can be overly complex for many use cases. EJS is one alternative does that job well and is very easy to set up.


* Setting up the Demo App: We will be making two pages for our application with one page with full width and the other with a sidebar.

    - package.json will hold our Node application information and the dependencies we need (express and EJS). server.js will hold our Express server setup, configuration. We’ll define our routes to our pages here.

    -  we will need is Express and EJS. Now we have to install the dependencies we just defined.

    - We also have to set EJS as the view engine for our Express application using app.set('view engine', 'ejs');

    - We’ll call those partials and define three files we’ll use across all of our site: head.ejs, header.ejs, and footer.ejs.

    - Syntax for including an EJS Partial Use <%- include('RELATIVE/PATH/TO/FILE') %> to embed an EJS partial in another file.
        * The hyphen <%- instead of just <% to tell EJS to render raw HTML.
        * The path to the partial is relative to the current file.

    - Go back into your server.js file and add the following inside your app.get('/') route.

    - The EJS partial has access to all the same data as the parent view. But be careful: If you are referencing a variable in a partial, it needs to be defined in every view that uses the partial or it will throw an error.


* Conclusion
EJS lets us spin up quick applications when we don’t need anything too complex. By using partials and having the ability to easily pass variables to our views, we can build some great applications quickly.




 