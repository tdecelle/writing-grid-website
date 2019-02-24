<template>
  <div class="writers">
    <input class="searchbar" v-model="searchterm"/>
    <button @click="search()">Click Me!</button>
    <List name="" type="writer" :json="writers"/>
  </div>
</template>

<script>
import {Component, Prop, Vue } from 'vue-property-decorator';
import Searchbar from '@/components/Searchbar.vue';
import ListItem from '@/components/ListItem.vue';
import List from '@/components/List.vue';
import WritersJSON from '@/data/writers.json';

@Component({
  components: {
    Searchbar,
    ListItem,
    List,
  },
  json: WritersJSON,
  methods: {
    search() {
      let filteredWriters = [];
      alert(this.$data.searchterm);
      // do your filtering here
      this.$data.writers = filteredWriters;
    },
  },
  data: () => {
    return {
      writers: WritersJSON.writers,
      searchterm: '',
    };
  },
})

export default class Writers extends Vue {}
</script>

<style scoped>

.searchbar {
  margin: 0px 0px 0px 0px;
}

</style>
