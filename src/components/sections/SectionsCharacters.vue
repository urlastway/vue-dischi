<template>
  <section>
      <div class="container">
          <div class="row">
                <SearchBar class="col-12" @searching="filterCharacters"/>
          </div>
          <div class="songslist row">
              <CardCharacter class="col-12 col-sm-4 col-lg-2 " v-for="(character, index) in charactersFilter" :key="index" :character="character"/>
          </div>
      </div>
  </section>
</template>

<script>

import axios from 'axios';
import CardCharacter from '../commons/CardCharacter';
import SearchBar from '../commons/SearchBar';

export default {
    name: 'SectionsCharacters',
    data(){
        return{
            characters: [],
            charactersFilter: [],
        };
    },
    components:{
        CardCharacter,
        SearchBar,
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            // handle success
            this.characters = response.data.response;
            this.charactersFilter = response.data.response;
        })
        .catch((error) => {
            // handle error
            console.log(error);
        })
    },
    methods: {
        filterCharacters(readComponent){
            this.charactersFilter = this.characters.filter((element) => element.genre.toLowerCase().includes(readComponent.toLowerCase()));
        },
    }
}
</script>

<style lang="scss" scoped>
    .songslist{
        justify-content: center;
    }
</style>