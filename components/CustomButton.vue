<template>
  <button
    :class="type"
    @click="onClick">
    {{ title }}
  </button>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Button',
    },
    onClick: {
      type: Function,
      default: () => null,
    },
    type: {
      type: String,
      default: 'default',
    },
  },
};
</script>

<style lang="sass" scoped>
button
  border: none
  color: black
  padding: 10px
  border-radius: 5px
  font-size: 1rem
  cursor: pointer

  &:focus
    outline: 0

.default
  background-color: #ecf0f1

  &:hover
    background-color: #bdc3c7

  &:active
    background-color: #7f8c8d

.primary
  background-color: #3498db
  color: white

  &:active
    background-color: #2980b9

.danger
  background-color: #e74c3c
  color: white

  &:active
    background-color: #c0392b
</style>
