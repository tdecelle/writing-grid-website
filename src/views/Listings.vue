<template>
  <div class="writers">
    <Searchbar class="searchbar"/>
    <List name="" type="listing" :json="$options.json.listings"/>
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
})

export default class Listings extends Vue {}
</script>

<style scoped>

.searchbar {
  margin: 0px 0px 0px 0px;
}

</style>
