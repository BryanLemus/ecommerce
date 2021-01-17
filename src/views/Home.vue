<template>
  <section-header title="New Arrivals" />
  <showcase>
    <card
      tag="Coming Soon"
      image="https://images-na.ssl-images-amazon.com/images/I/81ewD%2BorLSL._AC_SL1500_.jpg"
      title="LG 34WN780-B Pantalla Ergo de 34 pulgadas 21:9 UltraWide QHD (3440 x 1440) con diseño prácticamente sin bordes de 3 lados y AMD FreeSync, color negro"
      subtitle="by LG"
      price="$529.99"
      oldPrice="$699.99"
    />
    <card
      tag="New"
      image="https://images-na.ssl-images-amazon.com/images/I/81761uwFaIL._AC_SL1500_.jpg"
      title="MSI Gaming GeForce RTX 3070 8GB GDRR6 256-Bit HDMI/DP Tri-Frozr 2 TORX Fan 4.0 Amperio Arquitectura RGB OC Tarjeta gráfica (RTX 3070 Gaming X Trio)"
      subtitle="by MSI"
      price="$1199.00"
    />
    <card
      tag="Trending"
      image="https://images-na.ssl-images-amazon.com/images/I/71S3nPZ7uhL._AC_SL1500_.jpg"
      title="NZXT Kraken Z63 11.024 in - RL-KRZ63-01 - AIO RGB CPU Liquid Cooler - Pantalla LCD personalizable - Bomba mejorada - Alimentado por CAM V4 - Conector RGB - AER P 5.512 in Ventiladores de radiador (2 incluidas)"
      subtitle="by NZXT"
      price="$249.99"
    />
    <card
      tag="Editor's Choice"
      image="https://images-na.ssl-images-amazon.com/images/I/71Z5nDFMVNL._AC_SL1500_.jpg"
      title="ASUS ROG Thor 850 - Fuente de alimentación RGB completamente modular con panel OLED LiveDash"
      subtitle="by ASUS"
      price="$439.99"
    />
    <card
      tag="Best Seller"
      image="https://images-na.ssl-images-amazon.com/images/I/71LLczLHTxL._AC_SL1500_.jpg"
      title="Seagate Firecuda Gaming SSD - Unidad de disco externo de estado sólido"
      subtitle="by Seagate"
      price="$189.99"
      oldPrice="$220.99"
    />
    <card
      tag="Campaing"
      image="https://images-na.ssl-images-amazon.com/images/I/71WPGXQLcLL._AC_SL1384_.jpg"
      title="AMD Ryzen 5 3600 Procesador de escritorio desbloqueado de 6 núcleos y 12 hilos con Wraith Stealth Cooler"
      subtitle="by AMD"
      price="$199.99"
    />
    <card
      tag="Out of Sale"
      image="https://images-na.ssl-images-amazon.com/images/I/71Kkm5nIRKL._AC_SL1500_.jpg"
      title="Corsair Vengeance RGB PRO - Memoria de escritorio LED DDR4 de 3200 MHz C16 (16 GB, 2 x 8 GB), color negro"
      subtitle="by Corsair"
      price="$94.99"
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
