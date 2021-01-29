<template>
  <div id="Showcase" class="Showcase">
    <div class="Showcase-header">
      <subheader title="New Arrivals" />
      <Button @click="sLeft()">
        <i class="las la-arrow-left" />
      </Button>
      <Button @click="sRight()">
        <i class="las la-arrow-right" />
      </Button>
    </div>
    <div class="Showcase-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import Subheader from "./Subheader";
import Button from "./Button";

export default {
  name: "showcase",
  components: { Subheader, Button },
  methods: {
    sLeft() {
      document.getElementById("Showcase").scrollLeft -= 320;
    },
    sRight() {
      document.getElementById("Showcase").scrollLeft += 320;
    },
  },
};
</script>