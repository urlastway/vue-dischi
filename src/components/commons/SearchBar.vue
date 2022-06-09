<template>
  <div>
      <form class="gap-3" action="" @submit.prevent="$emit('searching', SearchText)">
          <input type="text" class="form-control" placeholder="Cerca un genere" v-model="SearchText">
          <button type="submit" class="btn btn-primary">Cerca</button>
          <button type="button" class="btn btn-warning">Resetta</button>
      </form>
  </div>
</template>

<script>
export default {
    name: 'SearchBar',
    data(){
        return{
            SearchText: '',
        }
    },
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