<template>
  <div class="Card">
    <dvi class="Card-image">
      <img :src="image"/>
    </dvi>
    <label class="Card-tag type-overline" :class="tagColor">{{ tag }}</label>
    <h6 class="Card-title">{{ title }}</h6>
    <label class="Card-subtitle type-subtitle1 text-gray-500">{{ subtitle }}</label>
    <label class="Card-price">{{ price }}</label>
    <label class="Card-oldPrice">{{ oldPrice }}</label>
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
        "Card-tag-campaign": this.tag === "Campaign",
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
