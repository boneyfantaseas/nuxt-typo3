<template functional>
  <video
    v-bind="data.attrs"
    :class="[data.class, data.staticClass]"
    class="t3-ce-media-video"
    controls
  >
    <source
      :src="props.file.publicUrl"
      :height="props.file.properties.dimensions.height"
      :width="props.file.properties.dimensions.width"
      :type="props.file.properties.mimeType"
    >
  </video>
</template>
<script>
export default {
  name: 'MediaVideo',
  functional: true,
  props: {
    file: {
      type: Object,
      required: true
    }
  }
}
</script>
