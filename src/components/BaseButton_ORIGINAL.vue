<template>
  <button :class="[$style.baseButton, $style[variant]]" v-bind="$attrs">
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
  padding: 0.6rem 1rem;
  color: var(--btn-text-color);
  background: var(--btn-bg-color);
}

.primary {
  --btn-text-color: var(--primary-text-color);
  --btn-bg-color: var(--primary-bg-color);
}

.secondary {
  --btn-text-color: var(--secondary-text-color);
  --btn-bg-color: var(--secondary-bg-color);
}

.warning {
  --btn-text-color: var(--warning-text-color);
  --btn-bg-color: var(--warning-bg-color);
}

.danger {
  --btn-text-color: var(--danger-text-color);
  --btn-bg-color: var(--danger-bg-color);
}
</style>
