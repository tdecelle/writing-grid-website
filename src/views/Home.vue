<template>
  <div class="home">
    <List name="Recent Edits" class="leftpane" type="edit" :json="edits"/>
    <!--<Homepage/>-->
    <div class="middlepane">
      <h1>Writing Grid</h1>
      <h3>Write - Edit - Connect</h3>
      <img src="../assets/writing-icon.png" alt="icon">
      <List name="Top Writers" type="writer" :json="writers"/>
    </div>
    <List name="New Job Listings" class="rightpane" type="listing" :json="listings" />
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

<style scoped>

.leftpane {
    width: 25%;
    height: 100%;
    float: left;
    border-collapse: collapse;
}

.middlepane {
    text-align: center;
    width: 34%;
    height: 100%;
    float: left;
    border-collapse: collapse;
}

.rightpane {
  width: 35%;
  height: 100%;
  position: relative;
  float: right;
  border-collapse: collapse;
}

img{
  width:230px;
}
</style>
