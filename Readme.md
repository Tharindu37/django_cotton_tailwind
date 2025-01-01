```
pip install -r requirements.txt
```
```
django-admin --version
```
```
django-admin startproject django_cotton
```
```
py manage.py runserver
```
```
py manage.py startapp cotton_ui
```

Install Tailwind CSS
```
npm init -y
```
```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init

```
```
module.exports = {
    content: [
        './templates/**/*.html',
        './static/**/*.js',
    ],
    theme: {
        extend: {},
    },
    plugins: [],
}

```
static/css/tailwind.css
```
@tailwind base;
@tailwind components;
@tailwind utilities;

```
```
"scripts": {
    "build:css": "npx tailwindcss -i ./static/css/tailwind.css -o ./static/css/output.css --watch"
}

npm run build:css
```
Load the generated output.css file in your base HTML template
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Django Project</title>
    <link rel="stylesheet" href="{% static 'css/output.css' %}">
</head>
<body>
    <!-- Content here -->
</body>
</html>

```
```
python manage.py runserver
```
Update the build:css script in package.json to optimize for production
```
"scripts": {
    "build:css": "npx tailwindcss -i ./static/css/tailwind.css -o ./static/css/output.css --minify"
}
```

```
taskkill /f /im python.exe
```