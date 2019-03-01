<template>
  <div class="listings">
    <div class="search">
      <h2>Search Job Listings</h2>
      <input type="text" v-on:keyup="search()" placeholder="Search..."  v-model="searchterm">
      <p>{{message}}</p>
      <List name="" type="listing" :json="displayed"/>
    </div>
    
    <div class="top">
      <List name="Top Job Listings" type="listing" :json="top_listings"/>
    </div>
  </div>
</template>

<script>
import {Component, Prop, Vue } from 'vue-property-decorator';
import Searchbar from '@/components/Searchbar.vue';
import ListItem from '@/components/ListItem.vue';
import List from '@/components/List.vue';
import ListingsJSON from '@/data/listings.json';

@Component({
  components: {
    Searchbar,
    ListItem,
    List,
  },
  json: ListingsJSON,
  methods: {
    search() {
      const listings = [];
      const searchterm = this.$data.searchterm;
      for (const l of this.$data.listings) {
        if (
          (l.company.toLowerCase().includes(searchterm) || l.title.toLowerCase().includes(searchterm))
          && searchterm !== '') {
          listings.push(l);
        }
      }
      if (listings.length === 0) {
        this.$data.message = 'No listings found.';
      } else {
        this.$data.message = '';
      }
      this.$data.displayed = listings;
    },
  },
  data: () => {
    return {
      listings: ListingsJSON.listings,
      displayed: [],
      top_listings: ListingsJSON.listings.slice(1, 7).reverse(),
      searchterm: '',
      message: '',
    };
  },
})

export default class Listings extends Vue {}
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
  background-color: #cccccc;
  border-radius: 25px;
  margin-top: 10px;
  float: left;
  width: 50%;
}
.top{
  float: right;
  width: 50%;
}

</style>