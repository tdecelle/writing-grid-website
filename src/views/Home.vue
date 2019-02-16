<template>
  <div class="home">
    <Homepage/>
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
