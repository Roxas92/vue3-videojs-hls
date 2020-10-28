<template>
	<video id="video" class="video-js" />
</template>

<script>
import videojs from 'video.js';
import 'video.js/dist/video-js.css';

export default {
name: 'App',
	mounted() {
		const element = document.getElementById('video');
		videojs(element, {
			controls: true,
			sources: [
				{
					src: 'https://music2memedia-euwe.streaming.media.azure.net/63697767-22a5-43c7-b8bd-a0667d896e1b/FINAL FANTASY XIV_ SHADOWBRINGER.ism/manifest(format=m3u8-cmaf)',
					type: 'application/x-mpegURL',
				},
			],
		});
	},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
