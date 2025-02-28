# Tailwind CSS Learning Journal

## Introduction

Tailwind CSS is a utility-first CSS framework that provides low-level utility classes to build custom designs without writing custom CSS. It allows you to rapidly build modern websites by composing small, reusable classes directly in your HTML.

## Getting Started

To add Tailwind CSS to your project, follow these steps:

1. **Install Tailwind CSS via npm:**
  ```bash
  npm install tailwindcss
  ```

2. **Create a configuration file:**
  ```bash
  npx tailwindcss init
  ```

3. **Configure your template paths:**
  In your `tailwind.config.js` file, add the paths to all of your template files:
  ```javascript
  module.exports = {
    content: [
     './src/**/*.{html,js}',
    ],
    theme: {
     extend: {},
    },
    plugins: [],
  }
  ```

4. **Add Tailwind directives to your CSS:**
  Create a CSS file (e.g., `style.css`) and add the following directives:
  ```css
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  ```

5. **Build your CSS:**
  Use the Tailwind CLI tool to process your CSS file:
  ```bash
  npx tailwindcss -i ./src/style.css -o ./dist/output.css --watch
  ```

6. **Include the generated CSS in your HTML:**
  Add a link to the generated CSS file in your HTML:
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tailwind CSS Example</title>
    <link href="/dist/output.css" rel="stylesheet">
  </head>
  <body>
    <div class="container mx-auto">
      <h1 class="text-4xl font-bold text-center mt-10">Hello, Tailwind CSS!</h1>
      <p class="text-center mt-4">This is a simple example of using Tailwind CSS.</p>
    </div>
  </body>
  </html>
  ```
