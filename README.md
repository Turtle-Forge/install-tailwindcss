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

# Tips-tips

### 1. Contoh struktur folder
![image](https://github.com/user-attachments/assets/8c2ff7b1-787b-4ca6-a097-4df6880b2431)

### 2. Start the Tailwind CLI build process dengan memasukan script nya ke dalam file package.json:
```
 "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "npx tailwindcss -i ./src/input.css -o ./src/output.css --watch"
  },
```
dan setelah pada saat start tailwind, gunakan perintah ini: ```npm run dev```

### 3. Terakhir jika dirasa sudah fix dan mau deploy maka simpan file css terakhir, yakni dengan perintah berikut ini:
```
npx tailwindcss -o ./public/css/style.css --minify
```
atau bisa memasukannya kedalam package.json seperti ```dev``` diatas yakni:
```
    "final": "npx tailwindcss -o ./public/css/style.css --minify"
```
dan dapat dijalankan dengan perintah ```npm run final```
