# ActiveMatch — static JavaScript adaptation

This archive contains only HTML, CSS, JavaScript and this README. It does not include Python, Django, Pyodide, WebAssembly or a backend.

## Deployment
Upload index.html and static/ to the root of a GitHub repository; enable Settings > Pages > Deploy from a branch > main / (root).

## Data model
All application state is held in JavaScript memory and resets on a page reload or new tab. No accounts or bookings are shared between visitors. Registration activates accounts immediately without email verification. The feature flags for magic links, coordinator approval and email confirmation are in static/demo.js.

## Important limitations
This is a browser-only functional adaptation, not a feature-perfect port of the Django application. The original server-side workflows (secure authentication, email, file uploads, payment processing, maps/geocoding, real-time chat, full administration and original database records) cannot be reproduced exactly by static hosting without reimplementing them or using an external service. Passwords are demo-only and held in memory as plain text; never use real passwords. No data survives a reload. The original CSS and Bootstrap assets are reused, but the views are reimplemented rather than directly rendered from Django templates.
