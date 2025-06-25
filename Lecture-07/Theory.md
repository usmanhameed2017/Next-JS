## Nested Layouts

- Next.js 15 uses the App Router (app/ directory) which supports nested layouts — allowing you to define shared UI (like headers/sidebars) that wrap around pages and even child layouts.

🔹 1. Basic Layout Setup
- Every route can have a layout.js file. It wraps the corresponding page and its children.

app/
 └──dashboard/
    ├──layout.js
    ├──page.js
    └──settings/
        ├──layout.js
        └──page.js

**app/dashboard/layout.jsx**
```javascript
export default function DashboardLayout({ children }) 
{
    return (
        <div>
            <Sidebar />
            <main> {children} </main>
        </div>
    );
}
```

**app/dashboard/settings/layout.jsx**
```javascript
export default function SettingsLayout({ children }) 
{
    return (
        <div>
            <h2>Settings</h2>
            {children}
        </div>
    );
}
```

🔹 3. Key Benefits
- Code reusability (headers/sidebars per section)

- Independent nested layouts

- Automatic layout persistence (no full page reload)