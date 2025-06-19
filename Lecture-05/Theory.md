## Route Groups

- In Next.js App Router, folders enclosed in round brackets (folderName) are called `group routes`. 

- They do not create their own route but are useful for organizing files.

- Lets us logically organize our routes and project files without impacting the URL structure.

- Let's implement authentication routes.

- `auth` folder must be enclosed by round brackets in order to exclude it from routing structure.

- (📂 **auth**) -> 📂 login -> 📜 page.jsx

- (📂 **auth**) -> 📂 signup -> 📜 page.jsx