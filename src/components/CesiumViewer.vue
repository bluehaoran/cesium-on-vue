<template>
    <div id="cesiumContainer"></div>
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

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

div#cesiumContainer {
  height: 100vh;
  width: 100vw;
}

</style>
