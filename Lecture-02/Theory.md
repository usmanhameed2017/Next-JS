## COMPONENTS

### Server Components

- By default, Next.js treats all components as Server components.

- These components can perform server-side tasks like reading files or fetching data directly from a database.

- The trade-off is that they can't use React hooks or handle user interactions.

### Client Components

- To create a Client component, you'll need to add the "use client" directive at the top of your component file. 

- While Client components can't perform server-side tasks like reading files. 

- They can use hooks and handle user interactions.

- Client components are the traditional React components you're already familiar with from previous versions of React.