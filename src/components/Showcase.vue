<template>
  <div class="showcase">
    <div class="showcase-header">
      <h2>{{ title }}</h2>
    </div>
    <div class="showcase-content">
      <card
        v-for="item in items"
        :index="index"
        :key="item.id"
        :image="item.image"
        :tag="item.tag"
        :name="item.name"
        :price="item.price"
        :oldPrice="item.oldPrice"
      />
    </div>
  </div>
</template>

<script>
import card from "./card";

export default {
  name: "showcase",
  components: {
    card
  },
  props: {
    title: String,
    items: []
  }
};
</script>
