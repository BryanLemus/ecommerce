<template>
  <div class="NumericUpDown">
    <label cladss="text-caption2">{{ label }}</label>
    <div class="NumericUpDown-content">
      <input
        v-model.number="inputValue"
        type="number"
        :max="max"
        :min="min"
        :step="step"
      />
      <div class="NumericUpDown-controls">
        <div class="noselect" @click="decrease()">
          <i class="fas fa-chevron-down" />
        </div>
        <div class="noselect" @click="increase()">
          <i class="fas fa-chevron-up" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NumericUpDown",
  data() {
    return {
      inputValue: this.value
    };
  },

  props: {
    label: String,
    value: { type: Number, default: 0 },
    max: { type: Number, default: Infinity },
    min: { type: Number, default: -Infinity },
    step: { type: Number, default: 1 }
  },

  methods: {
    increase() {
      if (this.inputValue < this.max) this.inputValue += this.step;
      else this.inputValue = this.max;
    },
    decrease() {
      if (this.inputValue > this.min) this.inputValue -= this.step;
      else this.inputValue = this.min;
    }
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/styles";
.NumericUpDown-content {
  display: flex;
  gap: 4px;
}
.NumericUpDown-controls {
  display: flex;
  div {
    background-color: hsl(0, 0%, 96%);
    padding: 0.5em 1em;
    &:hover {
      @include shadow-effect;
      background-color: hsl(0, 0, 99%);
      z-index: 1;
    }
    &:active {
      background: $blue-light;
      color: white;
    }
  }
}
</style>
