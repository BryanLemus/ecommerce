<template>
  <form class="Form" method="#">
    <div class="Form-header">
      <label class="text-headline">{{ title }}</label>
    </div>
    <div class="Form-content">
      <slot></slot>
    </div>
    <div class="Form-footer">
      <div class="Form-footer-controls">
        <input type="reset" class="btn-outline-primary" :value="cancelText" />
        <input type="submit" class="btn-primary" :value="submitText" />
      </div>
    </div>
  </form>
</template>

<script>
export default {
  name: "Form",
  props: {
    title: String,
    submitText: { type: String, default: "Send Request" },
    cancelText: { type: String, default: "Reset" }
  }
};
</script>
