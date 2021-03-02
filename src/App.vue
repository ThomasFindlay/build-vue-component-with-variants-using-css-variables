<template>
  <div :class="$style.container">
    <BaseButton variant="primary"> Primary </BaseButton>
    <BaseButton variant="secondary"> Secondary </BaseButton>
    <BaseButton variant="warning"> Warning </BaseButton>
    <BaseButton variant="danger"> Danger </BaseButton>
  </div>
</template>

<script>
import BaseButton from "./components/BaseButton.vue";
export default {
  components: {
    BaseButton,
  },
};
</script>

<style module>
.container {
  width: 300px;
  margin: 0 auto;
  display: grid;
  gap: 2rem;
  grid-template-columns: repeat(4, 1fr);
}
</style>
