<template>
  <div>
    <a-scene background="color: #ECECEC">
      <a-assets>
        <a-asset-item id="flyModel" src="https://cdn.aframe.io/test-models/models/glTF-2.0/virtualcity/VC.gltf"></a-asset-item>
      </a-assets>
      <a-entity gltf-model="#flyModel"></a-entity>
    </a-scene>
  </div>
</template>

<script>
export default {
  name: 'test',
  methods: {
    test() {

    }
  }
}
</script>
<style scoped>

</style>