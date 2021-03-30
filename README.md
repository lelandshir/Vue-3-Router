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

### JSON Server

- Simply exemplary as it's typical we get data from some API endpoint

```
mkdir data
touch db.json
npm i -g json-server
json-server --watch data/db.json
http://localhost:3000/jobs
```

### Working with Data/Waiting for Data

- Fetch/Promises, maybe use Axios?
- Render conditionally - good practice
- A popular place to get data is in the mounted lifecycle hook
- `Common Error:` Cannot find .whatver of null; because we don't have a value for the data reference until the mounted lifecycle hook has completed it's fetch request
- Use `v-if` directive and nest the elements responsible for rendering the data
