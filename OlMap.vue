<template>
  <div class="ol-map" :id="id"></div>
</template>

<script>
const ol = require('openlayers');
require('openlayers/dist/ol.css');

export default {
  name: 'ol-map',

  props: {
    lat: {
      required: true,
      type: Number
    },

    lon: {
      required: true,
      type: Number
    },

    zoom: {
      required: false,
      type: Number,
      default: 4
    }
  },

  data () {
    return {
      map: {
        type: Object,
        default: {}
      }
    }
  },

  computed: {
    id () {
      return this.$options.name + '-' + this._uid
    }
  },

  mounted () {
    this.map = new ol.Map({
      target: this.id,
      layers: [
        new ol.layer.Tile({
          source: new ol.source.OSM()
        })
      ],
      view: new ol.View({
        center: ol.proj.fromLonLat([this.lon, this.lat]),
        zoom: this.zoom
      })
    })
  }
}

</script>
