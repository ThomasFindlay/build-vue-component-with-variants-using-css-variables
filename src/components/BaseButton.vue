<template>
  <button :class="[$style.baseButton]" v-bind="$attrs">
    <slot />
  </button>
</template>

<script>
export default {
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
  background: transparent;
  padding: 0.6rem 1rem;
}

.primary {
}

.secondary {
}

.warning {
}

.danger {
}
</style>
