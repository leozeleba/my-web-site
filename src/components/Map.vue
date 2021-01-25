<template>

    <div style="height: 300px">
        <l-map
            :zoom="zoom"
            :center="center"
        >
            <l-tile-layer :url="url"></l-tile-layer>
            <l-marker :lat-lng="this.marker">
                <l-popup :content="map.address"></l-popup>
            </l-marker>
        </l-map>
    </div>
</template>

<script>
import "leaflet/dist/leaflet.css"
import {LMap, LTileLayer, LMarker, LPopup} from 'vue2-leaflet';

export default {
  components: {
    LMap,
    LTileLayer,
    LMarker,
    LPopup
  },
  data () {
    return {
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      zoom: 14,
      center: [this.map.longitude, this.map.latitude],
      marker: [this.map.longitude, this.map.latitude]
    };
  },
  methods: {
    zoomUpdated (zoom) {
      this.zoom = zoom;
    },
    centerUpdated (center) {
      this.center = center;
    },
    boundsUpdated (bounds) {
      this.bounds = bounds;
    }
  },
  props:{
      map: Object
  }
}
</script>

<style lang="scss" scoped>

</style>