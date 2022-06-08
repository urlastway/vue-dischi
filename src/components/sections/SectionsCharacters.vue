<template>
  <section>
      <div class="container">
          <div class="row">
              <div class="col-12 col-sm-6 col-lg-3" v-for="index in 12" :key="index"><CardCharacter/></div>
          </div>
      </div>
  </section>
</template>

<script>

import axios from 'axios';
import CardCharacter from '../commons/CardCharacter'

export default {
    name: 'SectionsCharacters',
    data(){
        return{
            characters: [],
        };
    },
    components:{
        CardCharacter
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