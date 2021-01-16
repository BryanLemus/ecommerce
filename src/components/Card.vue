<template>
  <div class="Card">
    <div class="Card-header">
      <label class="Card-tag" :class="tagColor">{{ tag }}</label>
      <div
        class="Card-favbtn"
        @click="isFavorite = !isFavorite"
        :class="{ 'Card-favbtn-checked': isFavorite }"
      />
    </div>
    <div class="Card-content">
      <div class="Card-image">
        <img v-bind:src="image" />
      </div>
      <h6 class="Card-title">{{ title }}</h6>
      <label class="Card-price">
        <label>{{ price }}</label>
        <label class="Card-oldPrice">{{ oldPrice }}</label>
      </label>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  data() {
    return {
      isFavorite: false
    };
  },
  computed: {
    tagColor: function() {
      return {
        "Card-tag-new": this.tag === "New",
        "Card-tag-bs": this.tag === "Best Seller",
        "Card-tag-cs": this.tag === "Coming Soon",
        "Card-tag-trend": this.tag === "Trending",
        "Card-tag-editor": this.tag === "Editor's Choice",
        "Card-tag-out": this.tag === "Out of Sale",
        "Card-tag-off": this.tag.includes("Off")
      };
    }
  },
  props: {
    image: {type: String, default: ''},
    tag: {type: String, default: ''},
    title: {type: String, default: ''},
    subtitle: {type: String, default: ''},
    price: {type: String, default: ''},
    oldPrice: {type: String, default: ''}
  }
};
</script>
