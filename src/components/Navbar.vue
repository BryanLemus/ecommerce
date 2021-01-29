<template>
  <div class="navbar" :class="{ 'navbar--search-mode': SearchOpened }">
    <a @click="$router.push('/')" class="navbar-logo">
      <img src="@/assets/images/logo-8.svg" />
    </a>
    <form class="navbar-search">
      <input type="search" :placeholder="placeholder" />
    </form>
    <div class="navbar-controls">
      <div
        id="close-button"
        class="navbar-button"
        @click="SearchOpened = false"
      >
        <i class="las la-angle-left" />
      </div>
      <div id="open-button" class="navbar-button" @click="SearchOpened = true">
        <i class="las la-search" />
      </div>
      <div class="navbar-button">
        <i class="las la-shopping-cart" />
        <subheader title="Cart" subtitle="0 items" />
      </div>
      <div class="navbar-button">
        <i class="las la-user-circle" />
        <subheader title="Sing in" :subtitle="username" />
      </div>
    </div>
  </div>
</template>

<script>
import subheader from "./Subheader";

export default {
  name: "navbar",
  data: function () {
    return {
      SearchOpened: false,
    };
  },
  components: {
    subheader,
  },
  props: {
    username: { type: String, default: "Sign in" },
    placeholder: String,
  },
};
</script>
