<template>
  <b-container class="bv-example-row">
    <b-row>
      <b-col cols="12" class="font-s">Account Balance</b-col>
    </b-row>
    <b-row>
      <b-col cols="6">
        <span class="currency">$$</span>
        <span>3245</span>
      </b-col>
      <b-col cols="6">
        <img src="@/assets/box.svg" />
        New Card
      </b-col>
    </b-row>
    <b-row>
      <b-tabs content-class="mt-3">
        <b-tab title="My Debit Cards" active>
          <b-carousel id="carousel1" indicators no-animation :interval="0">
            <b-carousel-slide img-blank>
              <CardView name="Mark Henry" />
            </b-carousel-slide>
            <b-carousel-slide img-blank>
              <CardView name="Glenn Mark" />
            </b-carousel-slide>
            <b-carousel-slide img-blank>
              <CardView name="Jurry San" />
            </b-carousel-slide>
          </b-carousel>
        </b-tab>
        <b-tab title="All Company Cards">
          <p>All Company card details</p>
        </b-tab>
      </b-tabs>
    </b-row>
  </b-container>
</template>


<script>
import CardView from "@/components/Card.vue";
export default {
  name: "HomeView",
  components: { CardView },
};
</script>

<style>
.font-s {
  text-align: left;
  font-family: "Open Sans";
}
.nav-tabs .nav-link.active,
.nav-tabs .nav-item.show .nav-link {
  color: white;
  border: none;
  border-bottom: 2px solid #23cefd !important;
  background: none;
}
.nav-tabs {
  border: none;
}
.nav-link {
  color: gray;
}

.nav-tabs .nav-link:hover,
.nav-tabs .nav-link:focus {
  border: none;
}

.currency {
  
}

.carousel-indicators li {
  box-sizing: content-box;
  flex: 0 1 auto;
  margin-right: 3px;
  margin-left: 3px;
  text-indent: -999px;
  cursor: pointer;
  background-color: #fff;
  background-clip: padding-box;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
  opacity: 0.5;
  transition: opacity 0.6s ease;
  height: 10px;
  width: 10px;
  border-radius: 50%;
  background-color: #01d167;
}

.carousel-indicators .active {
  opacity: 1;
  width: 25px;
  height: 10px;
  border-radius: 25px;
}
</style>
