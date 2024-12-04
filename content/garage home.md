# Garage Multi-App Setup Guide

## Project Structure
```
Garage/                      # Root repository
├── garage-home/            # Landing page app
│   ├── src/               # Source files
│   ├── dist/              # Build output
│   ├── package.json
│   └── vite.config.js
├── app-name/              # Your new app
│   ├── src/
│   ├── dist/
│   ├── package.json
│   └── vite.config.js
└── netlify.toml           # Deployment configuration
```

## Adding a New App

1. **Create New App**
   ```bash
   # In Garage directory
   npm create vite@latest app-name -- --template react
   cd app-name
   npm install
   ```

2. **Configure Vite**
   In your new app's `vite.config.js`:
   ```javascript
   export default defineConfig({
     plugins: [react()],
     base: '/app-name/',  // Must match the URL path
   })
   ```

3. **Update Landing Page**
   In `garage-home/src/App.jsx`, add your new app to the `apps` array:
   ```javascript
   const apps = [
     {
       title: "Your New App",
       description: "Description of your app",
       icon: YourIcon,  // Import from lucide-react
       link: "/app-name"
     },
     // ... existing apps
   ];
   ```

4. **Update Netlify Configuration**
   In `netlify.toml`, add your new app to the build process:
   ```toml
   [build]
     base = "garage-home"
     command = """
       npm run build && \
       cd ../shanty-generator && npm install && npm run build && \
       mkdir -p ../garage-home/dist/shanty && \
       cp -r dist/* ../garage-home/dist/shanty/ && \
       cd ../app-name && npm install && npm run build && \
       mkdir -p ../garage-home/dist/app-name && \
       cp -r dist/* ../garage-home/dist/app-name/
     """
     publish = "dist"

   [[redirects]]
     from = "/app-name/*"
     to = "/app-name/index.html"
     status = 200

   # ... existing redirects
   ```

5. **Commit and Deploy**
   ```bash
   git add .
   git commit -m "Add new app: app-name"
   git push
   ```

The new app will be automatically deployed to `garage.rudrakabir.com/app-name`

## Important Notes

- Each app must have a unique base path in its `vite.config.js`
- The base path must match:
  - The directory name
  - The path in netlify.toml redirects
  - The link in the landing page
- Always test the build locally before pushing:
  ```bash
  cd app-name
  npm run build
  ```

## Domain Configuration
- Main site: garage.rudrakabir.com
- Each app: garage.rudrakabir.com/app-name

## Troubleshooting

If deployment fails:
1. Check that the app name is consistent across all configurations
2. Verify all necessary dependencies are in package.json
3. Test the build locally first
4. Check Netlify logs for specific error messages

## Example: Adding a Calculator App

```bash
# Create new app
npm create vite@latest calculator -- --template react

# Update vite.config.js
export default defineConfig({
  plugins: [react()],
  base: '/calculator/',
})

# Update garage-home/src/App.jsx
import { Calculator } from 'lucide-react'

const apps = [
  {
    title: "Calculator",
    description: "A simple calculator app",
    icon: Calculator,
    link: "/calculator"
  },
  // ... existing apps
];

# Update netlify.toml with new build steps and redirects
```




# Prompt for my buddy claude
You're helping me with my Garage multi-app setup:
- Root repo (Garage/)
- garage-home as base (garage.rudrakabir.com landing)
- Apps in separate dirs, routed as /app-name
- Current netlify.toml:
[build]
  base = "garage-home"
  command = """
    npm run build && \
    cd ../shanty-generator && npm install && npm run build && \
    mkdir -p ../garage-home/dist/shanty && \
    cp -r dist/* ../garage-home/dist/shanty/
  """
  publish = "dist"
[[redirects]]
  from = "/shanty/*"
  to = "/shanty/index.html"
  status = 200
[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200

Each app needs:
- vite.config with base: '/app-name/'
- Entry in garage-home App.jsx apps array
- Build step in netlify.toml
- Redirect rule in netlify.toml