<template>
  <div id="app">
    <b-container class="bv-example-row">
      <b-row>
        <HeaderView />
      </b-row>
      <b-row>
        <router-view />
      </b-row>
      <b-row class="menu-bar">
        <ActionMenu />
      </b-row>
    </b-container>
  </div>
</template>

<script>
import ActionMenu from "@/components/ActionMenu.vue";
import HeaderView from "@/components/Header.vue";
export default {
  data() {},
  methods: {},
  components: {
    ActionMenu,
    HeaderView,
  },
};
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background-color: #0c365a;
}

.menu-bar {
  position: fixed;
  bottom: 0;
  width: 100%;
  -webkit-box-shadow: 0px -4px 3px #00000014;
  -moz-box-shadow: 0px -4px 3px #00000014;
  box-shadow: 0px -4px 3px #00000014;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
