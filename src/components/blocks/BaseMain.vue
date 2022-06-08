<template>
  <main class="main">
    <div class="main__padding">
      <SectionsCharacters/>
    </div>
  </main>
</template>

<script>

import SectionsCharacters from '../sections/SectionsCharacters';

export default {
    name: 'BaseMain',
    components:{
      SectionsCharacters
    },
}

</script>

<style lang="scss" scoped>
.main{
  background-color: var(--background__main__color);
  color: var(--main__title__color);

  &__padding{
    padding: 6rem 0;
  }
}
</style>