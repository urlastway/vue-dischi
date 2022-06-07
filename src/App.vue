<template>
  <div id="app">
    <BaseHeader/>
    <BaseMain/>
    <BaseFooter/>
  </div>
</template>

<script>
import BaseHeader from './components/blocks/BaseHeader';
import BaseMain from './components/blocks/BaseMain';
import BaseFooter from './components/blocks/BaseFooter';

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain,
    BaseFooter,
}
}
</script>

<style lang="scss">

@import './assets/style/global.scss';

</style>
