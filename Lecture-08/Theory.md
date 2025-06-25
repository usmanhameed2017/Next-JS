## 📘 Multiple Root Layouts

- In Next.js 15, you can define multiple root layouts using the App Router, allowing separate layout structures for different parts of your app.

- This is ideal for public vs admin dashboards, auth flows, etc.

🔹 1. What is a Root Layout?

- A layout.js file inside a top-level folder (like app/, app/admin/, etc.).

- Must include the <html> and <body> tags.

- Only one root layout per subtree.

app/
├── layout.js          ← Default root layout
├── page.js
├── admin/
│   ├── layout.js      ← Admin root layout
│   └── dashboard/
│       └── page.js
└── auth/
    ├── layout.js      ← Auth root layout
    └── login/
        └── page.js

**app/admin/layout.jsx**

```javascript
// app/admin/layout.js
export const metadata = { title: 'Admin Panel' };

export default function AdminLayout({ children }) 
{
    return (
        <html>
            <body>
                <Sidebar />
                {children}
            </body>
        </html>
    );
}
```