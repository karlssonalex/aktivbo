<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="list-group">
      <a href="#" class="list-group-item list-group-item-action">Dapibus ac facilisis in</a>


      <a href="#" class="list-group-item list-group-item-action list-group-item-primary">This is a primary list group item</a>
      <a href="#" class="list-group-item list-group-item-action list-group-item-secondary">This is a secondary list group item</a>
      <a href="#" class="list-group-item list-group-item-action list-group-item-success">This is a success list group item</a>
      <a href="#" class="list-group-item list-group-item-action list-group-item-danger">This is a danger list group item</a>
      <a href="#" class="list-group-item list-group-item-action list-group-item-warning">This is a warning list group item</a>
      <a href="#" class="list-group-item list-group-item-action list-group-item-info">This is a info list group item</a>
      <a href="#" class="list-group-item list-group-item-action list-group-item-light">This is a light list group item</a>
      <a href="#" class="list-group-item list-group-item-action list-group-item-dark">This is a dark list group item</a>
    </div>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
