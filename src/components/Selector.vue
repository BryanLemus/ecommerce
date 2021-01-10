<template>
  <div class="Selector">
    <div class="Selector-header">
      <label class="text-caption2">{{ label }}</label>
    </div>
    <div class="Selector-content">
      <div
        class="Selector-item"
        v-for="(item, index) in items"
        :key="item.id"
        @click="selected = index"
        :class="{ highlight: selected == index }"
      >
        {{ item.content }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Selector",
  data: function() {
    return {
      items: [
        { content: "512GB" },
        { content: "1TB" },
        { content: "2TB" },
        { content: "4TB" }
      ],
      selected: undefined
    };
  },
  props: {
    label: String
  }
};
</script>
