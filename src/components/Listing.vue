<template>
    <div>
        <h1>{{ listing }}</h1>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Listing extends Vue {
        @Prop() private listing!: object;
    }
</script>
<style scoped>

</style>