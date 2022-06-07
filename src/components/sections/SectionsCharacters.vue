<template>
  <section>
      
  </section>
</template>

<script>

import axios from 'axios';

export default {
    name: 'SectionsCharacters',
    data(){
        return{
            characters: [],
        };
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            // handle success
            this.characters = response.data;
        })
        .catch((error) => {
            // handle error
            console.log(error);
        })
    }
}
</script>

<style lang="scss" scoped>

</style>