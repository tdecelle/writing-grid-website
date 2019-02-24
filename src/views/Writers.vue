<template>
  <div class="writers">
    <Searchbar class="searchbar"/>
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
      alert(WritersJSON.writers);
      this.$data.writers = [this.$data.writers[0]];
    },
  },
  data: () => {
    return {
      writers: WritersJSON.writers,
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
