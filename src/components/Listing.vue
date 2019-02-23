<template>
    <div id="listing-item">
        <h2>{{ listing.company }}</h2>
        <h3>{{ listing.title }}</h3>
        <p>{{ listing.pay }} - {{ listing.date }}</p>
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
    #listing-item {
        text-align: left;
    }
</style>
