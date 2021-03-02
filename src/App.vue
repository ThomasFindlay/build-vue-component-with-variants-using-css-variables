<template>
  <div :class="$style.container">
    <BaseButton variant="primary"> Primary </BaseButton>
    <BaseButton variant="secondary"> Secondary </BaseButton>
    <BaseButton variant="warning"> Warning </BaseButton>
    <BaseButton variant="danger"> Danger </BaseButton>
  </div>
  <div :class="$style.container">
    <BaseTag variant="primary"> Primary </BaseTag>
    <BaseTag variant="secondary"> Secondary </BaseTag>
    <BaseTag variant="warning"> Warning </BaseTag>
    <BaseTag variant="danger"> Danger </BaseTag>
  </div>
</template>

<script>
import BaseButton from "./components/BaseButton.vue";
import BaseTag from "./components/BaseTag.vue";
export default {
  components: {
    BaseButton,
    BaseTag,
  },
};
</script>

<style module>
.container {
  width: 300px;
  margin: 2rem auto;
  display: grid;
  gap: 1.5rem;
  grid-template-columns: repeat(4, 1fr);
  justify-content: center;
}
</style>
