<template>
  <div class="SectionHeader">
    <h6 class="SectionHeader-title">{{ title }}</h6>
    <div class="SectionHeader-subtitle subtitle1 text-gray-600">{{ subtitle }}</div>
  </div>
</template>

<script>
export default {
  name: "SectionHeader",
  props: {
    title: {type: String, default: ''},
    subtitle: {type: String, default: ''},
  },
};
</script>

<style lang="scss" scoped>
.SectionHeader-title, .SectionHeader-subtitle{
display: -webkit-box;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
    overflow: hidden;
}
</style>