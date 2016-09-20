# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    Inside the ember application router is where you define where the routes
    will be, as in where the information is being taken to. That route
    computicates with the template to load the proper information. An ember
    route is what holds all the information pertaining to an object. It holds the information
    <!-- your response here -->
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
   ember generate route boston/campus
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first one routes to the product id on the product routes.
    The second one links to the product id on the products routes
    the first one involves nested routes where te product path is a child
    of the products route and is done so inside of a function where the nested route(child) as a function.
    The second one by looking at it I would think it is a child of a products route
    but I do not see products route above it. It is routing to the route of products
    associated with a specific ID. The first one. I think they are both correct,
    but the first one I have never seen before. But since it is happening inside the same route as products I think its legal
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
   By creating a property name where its value would be 123. 123 would be its
   movie_id
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
  we reference the data by concatinating the property name of the data with model
  wrapped in {{}} ie: {{model.age}} {{model.name}} {{model.title}}
    ```
