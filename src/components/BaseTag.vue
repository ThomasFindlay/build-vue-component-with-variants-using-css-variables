<template>
  <VariantStyleProvider :variant="variant">
    <template #default="{ variantStyle }">
      <div :class="[$style.baseTag, variantStyle]" v-bind="$attrs">
        <slot />
      </div>
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
.baseTag {
  border: none;
  border-radius: 1.5rem;
  padding: 0.6rem 1rem;
}
</style>
