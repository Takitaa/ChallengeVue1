<template>
  <div id="video-player">
    <!-- Include stylesheet -->
    <link
      href="https://cdn.jsdelivr.net/npm/video.js@6.6.2/dist/video-js.css"
      rel="stylesheet"
    />
    <link
      href="https://cdn.jsdelivr.net/npm/vue-video-player@5.0.0/src/custom-theme.css"
      rel="stylesheet"
    />
    <!-- Include the videojs library -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/video.js/6.6.2/video.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>
    <!-- videojs JS Vue -->
    <script src="https://cdn.jsdelivr.net/npm/vue-video-player@5.0.0/dist/vue-video-player.js"></script>

    <div id="app">
      <p>{{ message }}</p>
      <video-player
        class="vjs-custom-skin"
        ref="videoPlayer"
        :options="playerOptions"
        :playsinline="true"
        @play="onPlayerPlay($event)"
        @pause="onPlayerPause($event)"
        @ended="onPlayerEnded($event)"
        @loadeddata="onPlayerLoadeddata($event)"
        @waiting="onPlayerWaiting($event)"
        @playing="onPlayerPlaying($event)"
        @timeupdate="onPlayerTimeupdate($event)"
        @canplay="onPlayerCanplay($event)"
        @canplaythrough="onPlayerCanplaythrough($event)"
        @ready="playerReadied"
        @statechanged="playerStateChanged($event)"
      >
      </video-player>
    </div>
  </div>
  </div>
</template>
