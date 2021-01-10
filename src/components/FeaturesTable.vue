<template>
  <div class="FeaturesTable">
    <div class="FeaturesTable-Header">
      <h5 class="FeaturesTable-Header-Title">{{ title }}</h5>
      <div class="FeaturesTable-Header-Controls">
        <button class="btn-primary">Compare</button>
      </div>
    </div>
    <div class="FeaturesTable-Content">
      <div class="FeaturesTable-Item" v-for="item in items" :key="item.id">
        <div class="FeaturesTable-Item-Label">{{ item.name }}:</div>
        <div class="FeaturesTable-Item-Content">{{ item.content }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FeaturesTable",
  data() {
    return {
      items: [
        { name: "Brand", content: "NZXT" },
        { name: "Item model number", content: "RL-KRZ63-01" },
        { name: "Item Weight", content: "4.53 pounds" },
        { name: "Product Dimensions", content: "13.78 x 7.87 x 9.84 inches" },
        { name: "ASIN", content: "B084HLVZJ7" },
        { name: "Date First Available", content: "Febrary 5, 2020" }
      ]
    };
  },
  props: {
    title: String
  }
};
</script>
