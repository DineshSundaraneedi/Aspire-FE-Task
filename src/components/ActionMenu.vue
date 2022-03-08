<template>
  <b-nav>
    <b-nav-item v-for="(route, index) in config" v-bind:key="route.text">
      <div class="menu-item" v-on:click="() => navigate(index, route.path)">
        <img
          :src="
            route.active
              ? require(`@/assets/${route.activeIcon}`)
              : require(`@/assets/${route.inactiveIcon}`)
          "
        />

        <br />
        <span :class="[route.active ? 'activeCls' : '']">{{ route.text }}</span>
      </div>
    </b-nav-item>
  </b-nav>
</template>

<script>
export default {
  data() {
    return {
      config: [
        {
          activeIcon: "logo-active.svg",
          inactiveIcon: "logo-inactive.svg",
          text: "Home",
          path: "/",
          active: true,
        },
        {
          activeIcon: "pay.svg",
          inactiveIcon: "pay.svg",
          text: "Cards",
          path: "/cards",
          active: false,
        },
        {
          activeIcon: "Payments.svg",
          inactiveIcon: "Payments.svg",
          text: "Payments",
          path: "/payments",
          active: false,
        },
        {
          activeIcon: "Credit-inactive.svg",
          inactiveIcon: "Credit-inactive.svg",
          text: "Credit",
          path: "/credit",
          active: false,
        },
        {
          activeIcon: "Profile-inactive.svg",
          inactiveIcon: "Profile-inactive.svg",
          text: "Profile",
          path: "/profile",
          active: false,
        },
      ],
    };
  },
  methods: {
    navigate(index, path) {
      this.config.forEach((item) => (item.active = false));
      this.config[index].active = true;
      this.$router.push(path);
    },
  },
};
</script>

<style scoped>
.menu-item {
  font-size: 9px;
  color: #dddddd;
}
.menu-item img {
  height: 20px;
}
.nav{
  padding-left: 10px;
}
.nav-item{
  padding:0 5px;
}
.activeCls {
  color: #01d167;
}
</style>
