## Layouts

- Pages are `route-specific` UI components.

- A layout is UI that is shared between multiple pages in your app.

### How To Create Layouts

- Default export a React component from a `layout.js` or `layout.tsx` file.

- That component takes a `children` prop, which Next.js will populate with your page content.

- Add common components in your layout.jsx file.

```javascript
export const metadata = {
  title: 'Next Apps',
  description: 'Awesome Next.js app',
};

export default function RootLayout({ children }) {
    return (
        <html lang="en">
            <body>
                <header>
                    <h2> Header </h2>
                </header>
                
                {children}

                <footer>
                    <h2> Footer </h2>
                </footer>
            </body>
        </html>
    );
}
```