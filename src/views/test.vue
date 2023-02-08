<template>
  <div>
    <a-scene background="color: #ECECEC">
      <a-assets>
        <a-asset-item id="cityModel"
          src="https://cdn.aframe.io/test-models/models/glTF-2.0/virtualcity/VC.gltf"></a-asset-item>
      </a-assets>
      <a-entity gltf-model="#cityModel" play-all-model-animations modify-materials></a-entity>
    </a-scene>
  </div>
</template>

<script>
export default {
  name: 'test',
  methods: {
    test() {

    }
  },
  mounted: function () {
    console.log('mounted te'); 

    AFRAME.registerComponent('modify-materials', {
      init () {
        // Wait for model to load.
        this.el.setAttribute('gltf-model', 'https://cdn.aframe.io/test-models/models/glTF-2.0/virtualcity/VC.gltf')
        // this.el.setAttribute('gltf-model', '/assets/models/01.glb')
      }
    });
  }
}
</script>
<style scoped>

</style>