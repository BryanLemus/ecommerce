<template>
  <div class="Card">
    <img class="Card-image" :src="image" />
    <label class="Card-tag">{{ tag }}</label>
    <h6 class="Card-title">{{ title }}</h6>
    <label class="Card-subtitle subtitle1 text-gray-500">{{ subtitle }}</label>
    <label class="Card-price">{{ price }}</label>
    <label class="Card-oldPrice">{{ oldPrice }}</label>
    <div
      class="Card-favbtn"
      @click="isFavorite = !isFavorite"
      :class="{ 'Card-favbtn-checked': isFavorite }"
    />
  </div>
</template>

<script>
export default {
  name: "Card",
  data() {
    return {
      isFavorite: false,
    };
  },
  computed: {
    tagColor: function () {
      return {
        "Card-tag-new": this.tag === "New",
        "Card-tag-bs": this.tag === "Best Seller",
        "Card-tag-cs": this.tag === "Coming Soon",
        "Card-tag-trend": this.tag === "Trending",
        "Card-tag-editor": this.tag === "Editor's Choice",
        "Card-tag-out": this.tag === "Out of Sale",
        "Card-tag-off": this.tag.includes("Off"),
      };
    },
  },
  props: {
    image: { type: String, default: "" },
    tag: { type: String, default: "" },
    title: { type: String, default: "" },
    subtitle: { type: String, default: "" },
    price: { type: String, default: "" },
    oldPrice: { type: String, default: "" },
  },
};
</script>
