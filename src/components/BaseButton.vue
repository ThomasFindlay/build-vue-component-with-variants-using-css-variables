<template>
  <VariantStyleProvider :variant="variant">
    <template #default="{ variantStyle }">
      <button :class="[$style.baseButton, variantStyle]" v-bind="$attrs">
        <slot />
      </button>
    </template>
  </VariantStyleProvider>
</template>

<script>
import VariantStyleProvider from "./VariantStyleProvider.vue";

export default {
  components: {
    VariantStyleProvider,
  },
  props: {
    variant: {
      type: String,
      validators: value =>
        ["primary", "secondary", "warning", "danger"].includes(value),
    },
  },
};
</script>

<style module>
.baseButton {
  border: none;
  padding: 0.6rem 1rem;
}
</style>
