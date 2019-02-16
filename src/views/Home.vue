<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Homepage msg="Max's slogan should go here"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Homepage from '@/components/Homepage.vue'; // @ is an alias to /src

@Component({
  components: {
    Homepage,
  },
})
export default class Home extends Vue {}
</script>
