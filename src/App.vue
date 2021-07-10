<template>
  <VideoBg :sources="[video]">
    <Title msg="Welcome to tj-actions"/>
    <a href="https://github.com/tj-actions" class="button">Source on GitHub</a>
    <div id="social">
      <Title msg="Top Repositories"/>
      <div class="repo-item">
        <a class="repo" href="https://github.com/tj-actions/changed-files" target="_blank">changed files</a>
        <iframe src="https://ghbtns.com/github-btn.html?user=tj-actions&repo=changed-files&type=star&count=true&size=medium" frameborder="0" scrolling="0" width="170" height="30" title="GitHub"></iframe>
      </div>
      <div class="repo-item">
        <a class="repo" href="https://github.com/tj-actions/verify-changed-files" target="_blank">verify changed files</a>
        <iframe src="https://ghbtns.com/github-btn.html?user=tj-actions&repo=verify-changed-files&type=star&count=true&size=medium" frameborder="0" scrolling="0" width="170" height="30" title="GitHub"></iframe>
      </div>
      <div class="repo-item">
        <a class="repo" href="https://github.com/tj-actions/branch-names" target="_blank">branch-names</a>
        <iframe src="https://ghbtns.com/github-btn.html?user=tj-actions&repo=branch-names&type=star&count=true&size=medium" frameborder="0" scrolling="0" width="170" height="30" title="GitHub"></iframe>
      </div>
    </div>
  </VideoBg>
</template>

<script>
import VideoBg from 'vue-videobg'
import Title from './components/Title.vue'
import video from './assets/timelapse2.mp4'

export default {
  name: 'App',
  components: {
    Title,
    VideoBg
  },
  data: function () {
    return {
      video,
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.VideoBg {
  min-height: 640px;
}

.VideoBg__content {
  text-align: center;
  background-color: rgba(52, 72, 92, 0.7);
}

* {
  margin: 0;
}

img {
  width: 200px;
  margin-top: 120px;
}

h1, h4 {
  cursor: default;
}

a {
  text-decoration: none
}

h1 {
  margin: 40px 0;
  font-family: 'Dosis', 'Source Sans Pro', 'Helvetica Neue', sans-serif;
  font-weight: 300;
  font-size: 4em;
  color: #ebebeb;
}

h4, a {
  font-family: 'Source Sans Pro', 'Helvetica Neue', sans-serif;
  font-weight: 400;
  font-size: 15px;
  color: #7f8c8d;
}

.button {
  display: inline-block;
  width: 180px;
  margin: 0.5em;
  padding: 12px 14px;
  background-color: #4fc08d;
  font-weight: 700;
  color: #fff;
  border-bottom: 2px solid #3aa373;
  border-radius: 4px;
  -webkit-transition: all 0.15s ease;
  transition: all 0.15s ease;
}

.button:hover {
  background-color: #5dc596;
  -webkit-transform: translate(0, -2px);
  -ms-transform: translate(0, -2px);
  transform: translate(0, -2px);
}

#social {
  margin-top: 40px;
}

#social iframe {
  margin: -14px 4px;
}

#social a.repo {
  color: white;
  font-size: 20px;
}

#social div.repo-item {
  display: inline-block;
  margin: 0.5em;
  padding: 12px 14px;
  font-weight: 700;
  color: #fff;
  border-radius: 4px;
  -webkit-transition: all 0.15s ease;
  transition: all 0.15s ease;
}

#social div.repo-item:first-of-type {
  margin-left: 10em;
}

h2 {
  color: #fff;
}
</style>
