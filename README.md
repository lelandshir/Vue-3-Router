# Vue-3-Router:

### Jobs-Router

The way routes are handles in Vue seem to borrow from the JS Framework, Express

### About Vue Routes

- Routes is an `Array[]`
- Routes/succeeded by a /:id parameter will hit the item with the matching id similar to Express.JS
- Access the `id` of an object from another component using the `$route` obj

```
<h1>Job Details Page</h1>
<p>The job is {{ $route.params.id }}</p>
```

### Access \$routes obj via the component

- Pass route parameter to a URL by using the params prop, which is an obj

```
<router-link :to="{ name: 'JobDetails', params: { id: job.id } }">...
```

- Make dynamic router links that pass `$route.params`

### Redirects & 404

Push on an extra route to history

### History

The go method with a positive or negative integer

```
this.$router.go(1);
```
