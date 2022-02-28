<template>
  <div id="app">
    <!-- daqui -->
    <div id="video-player">
      <video
        class="video-js vjs-fill"
        autoplay
        controls
        preload="auto"
        data-setup="{}"
        loop
      >
        <source src="./assets/honda.mp4" type="video/mp4" />
        <p class="vjs-no-js">
          To view this video please enable JavaScript, and consider upgrading to
          a web browser that
          <a href="https://videojs.com/html5-video-support/" target="_blank"
            >supports HTML5 video</a
          >
        </p>
      </video>
    </div>
    <!-- div video-player-->
  </div>
</template>

<style></style>
