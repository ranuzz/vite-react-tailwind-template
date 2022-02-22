## Create the vite project

```sh
npm create vite@latest

# project_name 
# framework: react
# variant: react-ts
```

```sh
npm install
npm run dev
```

## Install tailwind

```sh
npm install -D tailwindcss postcss autoprefixer

npx tailwindcss init -p
```

## Update `tailwind.config.js`

```js
content: [
    "./index.html",
    "./src/**/*.{vue,js,ts,jsx,tsx}",
  ],
```

## add ./src/index.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Cleanup react scaffold

* remvoe image files
* Updare App.tsx and use tailwind with App.css

```css
.app-title {
  @apply text-3xl font-bold underline
}
```

```tsx
(
    <div>
        <h1 className="app-title">
        Hello world!
        </h1>
    </div>
)
```

## Install ESLint

```sh
npm install eslint --save-dev
npm init @eslint/config
```

```
✔ How would you like to use ESLint? · style
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · No / Yes
✔ Where does your code run? · browser
✔ How would you like to define a style for your project? · prompt
✔ What format do you want your config file to be in? · JavaScript
✔ What style of indentation do you use? · 4
✔ What quotes do you use for strings? · single
✔ What line endings do you use? · unix
✔ Do you require semicolons? · No / Yes
The config that you've selected requires the following dependencies:

eslint-plugin-react@latest @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser@latest
✔ Would you like to install them now with npm? · No / Yes
```

## Enforce ESLint on save

add file .vscode/settings.json
```json
{
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    },
    "eslint.validate": ["javascript"]
}
```