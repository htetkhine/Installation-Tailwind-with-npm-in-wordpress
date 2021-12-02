# Installation-Tailwind-with-npm-in-wordpress

# Tailwind Css
​
Rapidly build modern websites without ever leaving your HTML.
Learn More [Tailwind Website](https://tailwindcss.com/)
​
## Installation in wordpress
​
**Firstly NPM Package install**
​
```bash
npm init -y
```
​
**Install Tailwind PostCss and autoprefixer**
​
```bash
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest
```
​
**To change Tailwind Project**
​
```bash
npx tailwindcss init
```
​
**Combine file create**
​
```bash
assets/scss/style.scss
```
​
**style.scss combine to dist/style.css**
​
```bash
npx tailwindcss build .\assets\scss\style.scss -o .\assets\dist\css\style.css
```
​
**create laravel mix**
​
```bash
npm install laravel-mix --save-dev
```
​
**create webpack.mix.js file**
​
```bash
touch webpack.mix.js
```
​
**Define Your Compilation**
​
```bash
let mix = require('laravel-mix');
mix.js('assets/js/script.js', 'js')
    .sass('assets/scss/style.scss', 'css')
    .options({
        postCss: [
            require('tailwindcss')
        ],
    })
    .setPublicPath('assets/dist')
    .browserSync({
        server: './',
        files: ['./*.php', './dist'],
    });
```
​
**Compile**
​
```bash
npx mix
```
