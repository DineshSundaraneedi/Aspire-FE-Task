<template>
  <b-row>
    <div class="card-view">
      <div class="card-logo">
        <img src="@/assets/card-logo.svg" />
      </div>
      <p>{{ name }}</p>
    </div>
  </b-row>
</template>

<script>
export default {
  name: "CardView",
  props: {
    name: String,
  },
};
</script>

<style scoped>
.card-logo {
  align-items: flex-end;
  width: 25px;
  height: 25px;
}

.card-view {
  widows: 358px;
  height: 220px;
  background-color: #01d167;
  border-radius: 10px;
}
</style>
