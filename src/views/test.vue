<template>
  <div>
    <a-scene background="color: #ECECEC">
      <a-assets timeout="10000">
        <a-asset-item id="cityModel" src="/static/01.glb"></a-asset-item>
      </a-assets>
      <a-entity camera look-controls>
        <a-entity id='1' gltf-model="#cityModel" load-model position='2 0 -5' rotation='0 180 0' scale='0.2 0.2 0.2'></a-entity>
      </a-entity>
      <a-entity id='2' gltf-model="#cityModel" load-model position='2 2 -5' rotation='0 90 0' scale='0.2 0.2 0.2'></a-entity>
      <a-entity id='3' gltf-model="#cityModel" load-model position='5 2 -5' rotation='0 45 0' scale='0.2 0.2 0.2'></a-entity>
      <a-entity id='4' gltf-model="#cityModel" load-model position='5 0 -5' rotation='0 135 0' scale='0.1 0.1 0.1'></a-entity>

      <a-entity camera look-controls>
        <a-entity geometry="primitive: plane; height: 0.2; width: 0.2" position="0 0 -1"
                  material="color: gray; opacity: 0.5"></a-entity>
      </a-entity>
    </a-scene>
  </div>
</template>

<script>
import 'aframe'
export default {
  name: 'test',
  methods: {
    test() {

    }
  },
  mounted: function () {
    AFRAME.registerComponent('load-model', {
      init () {
        // Wait for model to load.
        this.el.setAttribute('gltf-model', '/static/01.glb')
      }
    });
  }
}
</script>
<style scoped>

</style>