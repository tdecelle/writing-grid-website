<template>
  <div class="writers">
    <Searchbar class="searchbar"/>
    <ListItem v-bind:key="writer" v-for="writer in $options.json.writers" :writer="writer" type="writer"/>
  </div>
</template>

<script>
import {Component, Prop, Vue } from 'vue-property-decorator';
import Searchbar from '@/components/Searchbar.vue';
import ListItem from '@/components/ListItem.vue';
import WritersJSON from '@/data/writers.json';

@Component({
  components: {
    Searchbar,
    ListItem,
  },
  json: WritersJSON,
})

export default class Writers extends Vue {}
</script>

<style scoped>

.searchbar {
  margin: 0px 0px 0px 0px;
}

</style>
