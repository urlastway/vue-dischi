<template>
  <div>
      <form action="">
          <input type="text" class="form-control" placeholder="Cerca un genere">
      </form>
  </div>
</template>

<script>
export default {
    name: 'SearchBar',
}
</script>

<style lang="scss" scoped>
    form{
        display: flex;
        justify-content: center;
        padding-bottom: 5rem ;
    }
    input{
        max-width: 60rem;
    }
</style>