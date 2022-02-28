<template>
  <div id="app">
    <div id="video-player">
      <vam-video
        :properties="videoOption.properties"
        :videoStyle="videoOption.videoStyle"
        :controlsConfig="videoOption.controlsConfig"
        @play="playVideo"
        @canplay="canplayVideo"
        @pause="pauseVideo"
      ></vam-video>
    </div>
  </div>
</template>

<script>
import VamVideo from "vue-vam-video";
export default {
  name: "App",
  components: {
    VamVideo,
  },
  data: () => ({
    videoOption: {
      properties: {
        src: "https://cdn.spect8.io/s8c/spect8.demo.background.video.v1.hq.mp4",

        // src: "./assets/grr.mp4",

        preload: "auto",
        loop: "loop",
        autoplay: "autoplay",
        muted: true,
      },
      videoStyle: {
        // width: "1200px",
        // height: "600px",
      },
      controlsConfig: {
        fullScreenTit: "全屏",
        EscfullScreenTit: "退出全屏",
        // speedTit: "倍速",
        // yinliangTit: "音量",
        // jingyinTit: "静音",
        playTit: "播放",
        pauseTit: "暂停",
        fullScreen: true,
        // speed: true,
        // listen: true,
      },
    },
  }),
  // methods: {
  //   playVideo() {
  //     console.log("play");
  //   },
  //   pauseVideo() {
  //     console.log("pause");
  //   },
  //   canplayVideo() {
  //     console.log("canplay");
  //   },
  // },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
