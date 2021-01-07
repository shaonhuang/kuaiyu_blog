<template>
  <div id="putInMiddle">
    <video width="400" height="800" controls>
      <source :src="normalizedVideoSrc" type="video/mp4" />
      您的浏览器不支持 HTML5 video 标签。
    </video>
  </div>
</template>

<script>
export default {
  name: "VideoPlayer",
  computed: {
    normalizedVideoSrc() {
      // console.log(this.$route.query.frg)
      if (this.$route.query.frg == 1) {
        return require("@/" + "assets/video/proteinrecorder2_2_带声音.mp4");
      } else if (this.$route.query.frg == 2) {
        return require("@/" + "assets/video/微信小程序展示视频.mp4");
        return;
      } else {
        return require("@/" + "assets/video/极客网演示视频.mp4");
      }
    },
  },
  methods: {},
};
</script>

<style>
#putInMiddle {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border: rgba(255, 255, 255, 0.609) 1px solid;
}
</style>
