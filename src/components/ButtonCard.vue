<script setup lang="ts">
type Props = { text: string };

defineProps<Props>();
</script>

<template>
  <div class="button">
    <span class="text">{{ text }}</span>
    <slot></slot>
  </div>
</template>

<style lang="scss">
.button {
  display: flex;
  height: 4rem;
  width: inherit;
  border: 2px solid #4f709c;
  border-radius: 8px;
  font-size: 1.5rem;
  justify-content: space-between;
  align-items: center;
  padding: 0 1rem;
}

@media screen and (max-width: $mobile) {
  .button {
    border-right: none;
    border-left: none;
    border-radius: 0;
  }
}
</style>
