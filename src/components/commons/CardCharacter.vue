<template>
  <div class="element">
      <img :src="character.poster" :alt="character.author">
      <h3 class="element__title">{{character.genre}}</h3>
      <h5 class="element__autor">{{character.year}}</h5>
      <h6 class="element__year">Anno</h6>
  </div>
</template>

<script>
export default {
    name: 'CardCharacter',
    props:{
        character: Object,
    },
}
</script>

<style lang="scss" scoped>
    .element{
        display: flex;
        align-items: center;
        flex-direction: column;
        padding: 2rem;
        padding-bottom: 2rem;
        background-color: var(--background__img__color);
        margin: 10px;
        
        &__title{
            font-size: 20px;
            padding-top: 1rem;
            text-transform: uppercase;
            text-align: center;
        }
        &__autor{
            font-size: 18px;
            text-align: center;
            color: var(--main__subtitle__color);
        }
        &__year{
            font-size: 16px;
            padding-top: 0.2rem;
            text-align: center;
            color: var(--main__subtitle__color);
        }
        img {
            max-width: 100%;
        }
    }
</style>