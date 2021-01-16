<template>
  <section-header title="New Arrivals" />
  <showcase>
    <card
      tag="Coming Soon"
      image="https://images-na.ssl-images-amazon.com/images/I/81ewD%2BorLSL._AC_SL1500_.jpg"
      title="LG 34WN780-B Pantalla Ergo de 34 pulgadas 21:9 UltraWide QHD (3440 x 1440) con diseño prácticamente sin bordes de 3 lados y AMD FreeSync, color negro"
      subtitle="by LG"
      price="529.99"
      oldPrice="699.99"
    />
  </showcase>
  <section-header title="Offers" />
  <showcase>
    <card />
    <card />
    <card />
    <card />
    <card />
    <card />
    <card />
  </showcase>
  <section-header title="Top Trending" />
  <showcase>
    <card />
    <card />
    <card />
    <card />
    <card />
    <card />
    <card />
  </showcase>
  <section-header title="Best Sellers" />
  <showcase>
    <card />
    <card />
    <card />
    <card />
    <card />
    <card />
    <card />
  </showcase>
</template>

<script>
import Card from "../components/Card.vue";
import SectionHeader from "../components/SectionHeader.vue";
import Showcase from "./../components/Showcase";

export default {
  name: "Home",
  components: { Showcase, Card, SectionHeader },
};
</script>
