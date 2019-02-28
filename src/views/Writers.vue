<template>
  <div class="writers">
    <div class="search">
      <h2>Search Writers</h2>
      <input type="text" v-on:keyup="search()" placeholder="Search..."  v-model="searchterm" class="round">
      <p>{{message}}</p>
      <List name="" type="writer" :json="displayed"/>
    </div>
    
    <div class="top">
      <List name="Top Writers" type="writer" :json="top_writers"/>
    </div>
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
      const writers = [];
      const searchterm = this.$data.searchterm;

      for (const w of this.$data.writers) {
        if (w.name.toLowerCase().includes(searchterm) && searchterm !== '') {
          writers.push(w);
        }
      }
      if (writers.length === 0) {
        this.$data.message = 'No writers found.';
      } else {
        this.$data.message = '';
      }

      this.$data.displayed = writers;
    },
  },
  data: () => {
    return {
      writers: WritersJSON.writers,
      displayed: [],
      top_writers: WritersJSON.writers.slice(1, 7).reverse(),
      searchterm: '',
      message: '',
    };
  },
})

export default class Writers extends Vue {}
</script>

<style scoped>

input[type=text] {
  background-color: white;
  background-repeat: no-repeat;
  width:50%;
  margin: 10px;
}

.search{
  text-align:center;
  background-color: #b7b7b7;
  border-radius: 25px;
  margin-top: 10px;
  float: left;
  width: 50%;
}
.top{
  float: right;
  width: 50%;
}

input {
    width: 100%;
    border-radius: 15px;
    border: 1px #000 solid;
    padding: 5px 5px 5px 25px;
    top: 0;
    left: 0;
    z-index: 5;
    outline: none;
}
</style>
