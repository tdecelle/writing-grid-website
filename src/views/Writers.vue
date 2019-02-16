<template>
  <div class="writers">
    <Searchbar/>
  </div>
</template>

<script lang="ts">
import {Component, Prop, Vue } from 'vue-property-decorator';
import Searchbar from '@/components/Searchbar.vue';

@Component({
  components: {
    Searchbar,
  },
})
export default class Writers extends Vue {
  @Prop() private msg!: string;
}

</script>

<style scoped>

</style>
