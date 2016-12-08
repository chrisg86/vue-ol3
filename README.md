# vue-ol3
Use openlayers 3 with vuejs

# Usage
Use it like this in your `App.vue` file:

```
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
```
import Vue from 'vue'
import App from './App'

/* eslint-disable no-new */
new Vue({
  el: '#app',
  template: '<App/>',
  components: { App }
})
```
