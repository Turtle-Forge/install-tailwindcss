# install-tailwindcss
### 1. Install
1. Buka direktori project
2. inisialisasi npm :
   ```
   npm init -y
   ```
4. install tailwindcss, postcss, dan autoprefixer :
   ```
   npm install -D tailwindcss postcss autoprefixer
   ```
5. ```
   npx tailwindcss init
   ```

### 2. Konfigurasi
``tailwind.config.js``

```
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 3. Add the Tailwind directives to your CSS
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 4. Start the Tailwind CLI build process
```
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```
### 5. Start using Tailwind in your HTML
- hubungkan file output css yang dihasilkan tailwind kedalam tag head html seperti menghubungkan css biasa:
  ```
  <link href="./output.css" rel="stylesheet">
  ```

### 6. Tailwind sudah bisa digunakan
```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
