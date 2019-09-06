# vue-game

## Build issue
Seeing an issue where the routes to the CSS, JS, and image files in index.html are not being found locally or on Connect. I have fixed it by adding a period to any references to thoughs files (this is a stackoverflow question). This is related to the build not using base urls

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
