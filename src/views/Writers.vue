<template>
  <div class="writers">
    <Searchbar class="searchbar"/>
    <Writer v-bind:key="writer" v-for="writer in $options.json.writers" :name="writer.name"/>
  </div>
</template>

<script>
import {Component, Prop, Vue } from 'vue-property-decorator';
import Searchbar from '@/components/Searchbar.vue';
import Writer from '@/components/Writer.vue';
import WritersJSON from '@/data/writers.json';

@Component({
  components: {
    Searchbar,
    Writer,
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
