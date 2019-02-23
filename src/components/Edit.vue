<template>
    <div>
        <h1>{{ edit }}</h1>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Edit extends Vue {
        @Prop() private edit!: object;
    }
</script>

<style scoped>

</style>