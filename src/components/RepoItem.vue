<template>
  <div class="repo-item">
    <a class="repo" v-bind:href="`https://github.com/tj-actions/${repoSha}`" target="_blank">{{ repository }}</a>
    <iframe v-bind:src="`https://ghbtns.com/github-btn.html?user=tj-actions&repo=${repoSha}&type=star&count=true&size=medium`" loading="lazy" frameborder="0" scrolling="0" width="170" height="30" title="GitHub"></iframe>
  </div>
</template>

<script>
export default {
  props: {
    repository: String,
    repoSha: String
  }
}
</script>

