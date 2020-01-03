<template>
    <div id="cesiumContainer">
        
    </div>
</template>

<script>
import { Cesium3DTileset, createWorldTerrain, IonResource, Viewer, viewerCesiumNavigationMixin } from 'cesium';
import "cesium/Build/Cesium/Widgets/widgets.css";
// import "./css/main.css";

export default {
  name: 'CesiumViewer',
  props: {
    msg: String
  },
  mounted: () => {
      var viewer = new Viewer('cesiumContainer', {
          terrainProvider: createWorldTerrain()
      });

      var tileset = new Cesium3DTileset({
          url: IonResource.fromAssetId(40866)
      });

      viewer.scene.primitives.add(tileset);
      viewer.zoomTo(tileset);
  }
}



// This is simplified version of Cesium's Getting Started tutorial.
// See https://cesium.com/docs/tutorials/getting-started/ for more details.

let defaultAccessToken = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqdGkiOiJmM2QzZjc1ZC02MTY2LTRjZTYtOWRjMi1jNGFhM2VjZmU2MDMiLCJpZCI6MjI3MSwic2NvcGVzIjpbImFzciIsImdjIl0sImlhdCI6MTU2MjAzNzY0OH0.XevWLMLJO8EcCq7-lyRG8lN3a01f52IjFze4rPBqTxI';

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
