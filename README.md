# Reactive Toolkit

Reactive Toolkit is a collection of custom hooks for building React applications.

## Install

```bash
npm install reactive-toolkit
```

### useFetchRT

```jsx
import useFetchRT from "reactive-toolkit";

function MyComponent() {
  const { data, isLoading, error } = useFetchRT(
    "https://jsonplaceholder.typicode.com/posts"
  );

  if (isLoading) {
    return <div>Loading...</div>;
  }

  if (error) {
    return <div>Error: {error}</div>;
  }

  return (
    <div>
      {data?.map((post) => (
        <div key={post.id}>
          <h2>{post.title}</h2>
          <p>{post.body}</p>
        </div>
      ))}
    </div>
  );
}
export default MyComponent;
```

## License

The MIT License.
