# spark.ui
Beautiful Blazor components made with Tailwind CSS.

## How to use
spark.ui components are meant to be copy and pasted into your Blazor project. This way you own the code and customize them as you see fit.

## Install spark.ui with Blazor or Spark.NET

### 1. Add Tailwind CSS to your project
Components are styled using Tailwind CSS. You will need to install Tailwind CSS in your Blazor projects root directory.

```
npm install -D tailwindcss @tailwindcss/forms
```

### 2. Add configs and components
Download the configs and components. Then unzip and paste them into the root of your project.

[Download Components](http://ui.spark-framework.net/spark-ui.zip)

The following is what you should have pasted in the root of your project.

- Components/**/*
- Styles/globals.css
- postcss.config.js
- tailwind.config.js

> Why not a Nuget package?
> 
> spark.ui is meant to be a lightweight, customizable, starting point for your next apps design. The code is yours. Copy, Paste, and Edit as you need.
>

### 3. Add css file reference
The `Styles/globals.css` file gets compiled into `/wwwroot/css/styles.css`.

You need to add a reference to the styles.css in the head tag of your layout file.

We also recommend to add a reference to the inter font family. It's what is used in the examples on this website.
```
<head>
...
<link href="https://rsms.me/inter/inter.css" rel="stylesheet" />
<link href="/css/styles.css" rel="stylesheet" />
...
</head>
```

### 4. Add namespaces to your projects _Imports.razor
```
@using Spark.UI.Components
@using [YourProjectName].Components
@using [YourProjectName].Components.Icons
@using [YourProjectName].Components.Typography
```

### 5. Start the Tailwind CLI build process
Run the Tailwind CLI tool to scan your template files for classes and build your public CSS file.
```
npx tailwindcss -i ./Styles/globals.css -o ./wwwroot/css/styles.css --watch
```
