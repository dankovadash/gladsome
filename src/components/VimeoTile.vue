<template>
<div :class="getContainerClass(ratio)">
  <iframe
    class="video"
    :src="`https://player.vimeo.com/video/${video}`"
    frameborder="0"
    allow="fullscreen; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    props: {
        video: String,
        ratio: String
    },
    methods: {
      getContainerClass(ratio) {
        return {
          '16:9': 'video-16-9',
          '4:5': 'video-4-5',
          '1:1': 'video-1-1'
        }[ratio];
      }
    }
})
</script>

<style scoped>
.video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.video-16-9 {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 56.25%;
}
.video-1-1 {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 100%;
}
.video-4-5 {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 125%;
}
</style>
