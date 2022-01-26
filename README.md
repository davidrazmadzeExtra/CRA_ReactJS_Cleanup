# Cleanup after running ‘create-react-app’

Create a new app using `create-react-app`. Read more about that here: https://create-react-app.dev
`npx create-react-app your-app-name-here`

## 1. Remove all unnecessary files

1. `.` - root of the directory
2. `/public`
3. `/src`

Run the following commands to remove all files that we won't be needing

1. `rm README.md`
2. `rm public/favicon.ico public/logo192.png public/logo512.png`
3. `rm src/App.test.js src/logo.svg src/reportWebVitals.js src/setupTests.js`

## 2. Edit some files

### 1. `public/index.html`

- Remove the following lines:

  5: `<link rel="icon" href="%PUBLIC_URL%/favicon.ico" />`
  
  12: `<link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />`

  And the comments in between `<!-- -->`

- Edit the title `<title> </title>`

- Edit the description:

```
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
```

- Look up some `HTML5` tags and tricks you could do to add in

### 2. `public/manifest.json`

Remove `icons`:

```json
  "icons": [
    {
      "src": "favicon.ico",
      "sizes": "64x64 32x32 24x24 16x16",
      "type": "image/x-icon"
    },
    {
      "src": "logo192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
    {
      "src": "logo512.png",
      "type": "image/png",
      "sizes": "512x512"
    }
  ],
```

### 3. `src/App.css`

Remove everything below line 4:

```js
.App {
  text-align: center;
}
```

### 4.`src/App.js`

- Remove the logo import:

`import logo from './logo.svg';`

- Remove everything inside the main `div` so that you are left with:

```
function App() {
  return (
    <div className="App">
    </div>
  );
}
```

### 5. `src/index.js`

- Remove web vitals reporting:

`import reportWebVitals from './reportWebVitals';`

```json
// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```
