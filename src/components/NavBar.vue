<template lang="pug">

nav.navbar(role='navigation' aria-label='main navigation')
  #navbarBasicExample.navbar-menu
    .navbar-start
      a.navbar-item
        router-link(to='/') Home
      a.navbar-item
        router-link(to='/about') About
      .navbar-item.has-dropdown.is-hoverable
        a.navbar-link
          | More
        .navbar-dropdown
          a.navbar-item
            router-link(to='/about') About
          hr.navbar-divider
          a.navbar-item
            router-link(to='/about') About
    .navbar-end
      .navbar-item
        .buttons
          a.button.is-primary
            strong Sign up
          a.button.is-light
            | Log in

</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
