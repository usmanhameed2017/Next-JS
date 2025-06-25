## Routing Metadata

- The Metadata API in Next.js is a powerful feature that lets us define metadata for each page.

- Metadata ensures our content looks great when it's shared or indexed by search engines.

- Two ways to handle metadata in layout.jsx files:

1. export a static metadata object
2. export a dynamic generateMetadata function

### Configuring metadata

**Metadata rules**

- Both layout.jsx and page.jsx can export metadata. Layout metadata applies to all its pages, while page metadata is specific to that page.

- Metadata follows a top-down order, starting from the root level.

- When metadata exists in multiple places along a route, they merge together, with page metadata overriding layout metadata for matching properties.