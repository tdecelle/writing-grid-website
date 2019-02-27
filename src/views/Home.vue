<template>
  <div class="home">
    <List name="Top Edits" type="edit" :json="edits"/>
    <Homepage/>
    <List name="Top Writers" type="writer" :json="writers"/>
    <List name="Top Listings" type="listing" :json="listings" />
  </div>
</template>

<script>
  import { Component, Vue } from 'vue-property-decorator';
  import Homepage from '@/components/Homepage.vue'; // @ is an alias to /src
  import List from '@/components/List.vue';
  import ListingsJSON from '@/data/listings.json';
  import EditsJSON from '@/data/edits.json';
  import WritersJSON from '@/data/writers.json';

  @Component({
    components: {
      Homepage,
      List,
    },
    data: () => {
      return {
        writers: WritersJSON.writers,
        listings: ListingsJSON.listings,
        edits: EditsJSON.edits,
      };
    },
  })
  export default class Home extends Vue {}
</script>
