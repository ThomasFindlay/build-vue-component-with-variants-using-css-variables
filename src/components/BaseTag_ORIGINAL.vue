<template>
  <div :class="[$style.baseTag, $style[variant]]" v-bind="$attrs">
    <slot />
  </div>
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
.baseTag {
  border: none;
  border-radius: 1.5rem;
  padding: 0.6rem 1rem;
  font-size: 1rem;
  color: var(--tag-text-color);
  background: var(--tag-bg-color);
}

.primary {
  --tag-text-color: var(--primary-text-color);
  --tag-bg-color: var(--primary-bg-color);
}

.secondary {
  --tag-text-color: var(--secondary-text-color);
  --tag-bg-color: var(--secondary-bg-color);
}

.warning {
  --tag-text-color: var(--warning-text-color);
  --tag-bg-color: var(--warning-bg-color);
}

.danger {
  --tag-text-color: var(--danger-text-color);
  --tag-bg-color: var(--danger-bg-color);
}
</style>
