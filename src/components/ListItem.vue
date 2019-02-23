<template>
    <div>
        <Writer v-if="type == 'writer'" :writer="writer"/>
    </div>
</template>

<script lang="ts">
import {Component, Prop, Vue } from 'vue-property-decorator';
import Writer from '@/components/Writer.vue';

@Component({
  components: {
      Writer,
  },
})

export default class ListItem extends Vue {
    @Prop() private type!: string;
    @Prop() private writer!: object;
}
</script>

<style scoped>

</style>