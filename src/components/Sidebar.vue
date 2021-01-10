<template>
  <div class="sidebar">
    <div class="sidebar-header">
      <div class="text-title2">{{ title }}</div>
    </div>
    <div class="sidebar-content">
      <ul class="sidebar-items" style="list-style-type: none">
        <li
          class="sidebar-item"
          v-for="(cat, index) in categories"
          :key="cat.id"
          @click="selected = index"
          :class="{ highlight: selected == index }"
        >
          {{ cat.name }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "sidebar",
  data: function() {
    return {
      categories: [
        { id: 1, name: "Computers" },
        { id: 2, name: "Electronics" },
        { id: 3, name: "Home & Living" },
        { id: 4, name: "Kitchen" },
        { id: 5, name: "Office" },
        { id: 6, name: "Education" },
        { id: 7, name: "Garage" },
        { id: 8, name: "Industrial" },
        { id: 9, name: "Plumbing" },
        { id: 10, name: "Locksmith" },
        { id: 11, name: "Outdoors" },
        { id: 12, name: "Luggage" },
        { id: 13, name: "Arts & Craft" },
        { id: 14, name: "Kids" }
      ],
      selected: undefined
    };
  },
  props: {
    title: String
  }
};
</script>
