<template>
  <section>
      <div class="container">
          <div class="songslist row">
              <CardCharacter class="col-12 col-sm-4 col-lg-2 " v-for="(character, index) in characters.response" :key="index" :character="character"/>
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
    .songslist{
        justify-content: center;
    }
</style>