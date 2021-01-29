<template>
  <div class="Subheader">
    <h6 class="Subheader-title">{{ title }}</h6>
    <div class="Subheader-subtitle type-subtitle1 text-gray-600">{{ subtitle }}</div>
  </div>
</template>

<script>
export default {
  name: "Subheader",
  props: {
    title: {type: String, default: ''},
    subtitle: {type: String, default: ''},
  },
};
</script>

<style lang="scss" scoped>
.Subheader-title, .Subheader-subtitle{
display: -webkit-box;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
    overflow: hidden;
}
</style>