# Vue-3-Router:

### Jobs-Router

The way routes are handles in Vue seem to borrow from the JS Framework, Express

- Routes is an `Array[]`
- Routes/succeeded by a /:id will hit the item with the matching id similar to Express.JS
- Access the `id` of an object from another component using the route object

```
<h1>Job Details Page</h1>
<p>The job is {{ $route.params.id }}</p>
```
