<template>
  <div class="element">
      <img src="https://image.shutterstock.com/image-vector/no-image-vector-symbol-missing-260nw-1310632172.jpg">
      <h3 class="element__title">Titolo</h3>
      <h5 class="element__autor">Autore</h5>
      <h6 class="element__year">Anno</h6>
  </div>
</template>

<script>
export default {
    name: 'CardCharacter',
}
</script>

<style lang="scss" scoped>
    .element{
        display: flex;
        flex-direction: column;
        padding: 2rem;
        padding-bottom: 2rem;
        background-color: var(--background__img__color);
        margin: 10px;
        
        &__title{
            padding-top: 1rem;
            text-transform: uppercase;
            text-align: center;
        }
        &__autor{
            text-align: center;
            color: var(--main__subtitle__color);
        }
        &__year{
            padding-top: 0.2rem;
            text-align: center;
            color: var(--main__subtitle__color);
        }
    }
</style>