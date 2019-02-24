<template>
  <div class="writers">
    <Searchbar class="searchbar" v-model="searchterm" v-bind="message"/>
    <p>{{message}}</p>
    
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
    onSearch: function(query, found) {
        this.$store.dispatch('search', query.value);
    },
    search() {
      
      var writers = [];
      // var search = this.$refs["#search"]
      alert(searchterm)
      
      // for (var w of this.$data.writers){
      //   if w.name.includes(search){
      //     writers.push(w);
      //   }
      // }
      
      this.$data.writers = writers;
      
      wthis.$data.writers = [this.$data.writers[0]];
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
