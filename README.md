# vue-ol3
Use openlayers 3 with vuejs. At this point you can only show a map at the given coordinates and zoom level.

```vue
<ol-map :lat="51.22" :lon="7.60"></ol-map>
```

# Usage
Use it like this in your `App.vue` file:

```vue
<template>
 <div id="app">
   <ol-map :lat="51.22" :lon="7.60"></ol-map>
 </div>
</template>

<script>
import OlMap from './components/OlMap'

export default {
  name: 'app',
  components: {
    OlMap
  }
}
</script>
```

And then like this in your `main.js` file:
```javascript
import Vue from 'vue'
import App from './App'

/* eslint-disable no-new */
new Vue({
  el: '#app',
  template: '<App/>',
  components: { App }
})
```
