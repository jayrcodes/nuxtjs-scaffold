<template>
  <section class="container">
    <h1>Test</h1>
    <p class="message">{{ $t('home.introduction') }}</p>
    <custom-button
      :on-click="test"
      :title="$t('links.sampleButton')"
      type="primary"
    />
  </section>
</template>

<script>
import CustomButton from '../components/CustomButton';

export default {
  components: {
    CustomButton,
  },
  methods: {
    test() {
      // eslint-disable-next-line
      alert('hello world');
    },
  },
};
</script>

<style lang="sass">
*
  font-family: sans-serif
</style>
