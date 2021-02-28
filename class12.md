# What I learned 



## EJS PARTIALS

![ejs](https://i.morioh.com/201120/f9bf1c1b.webp)

### Partials

When using the default view engine (ejs), Sails supports the use of partials (i.e. “view partials”). Partials are basically just views that are designed to be used from within other views.

They are particularly useful for reusing the same markup between different views, layouts, and even other partials.

* Example:
    - app.js
        * app.set('views', path.join(__dirname, 'views')); app.set('view engine', 'ejs');
    - error.ejs
        * <% include ./base/header %> <h1> Other mark up here </h1> <% include ./base/footer %>




### Notes

* Partials are rendered synchronously, so they will block Sails from serving more requests until they’re done loading. It’s something to keep in mind while developing your app, especially if you anticipate a large number of connections.

* Built-in support for partials in Sails is only for the default view engine, ejs. If you decide to customize your Sails install and use a view engine other than ejs, then please be aware that support for partials (sometimes known as “blocks”, “includes”, etc.) may or may not be included, and that the usage will vary. Refer to the documentation for your view engine of choice for more information on its syntax and conventions.