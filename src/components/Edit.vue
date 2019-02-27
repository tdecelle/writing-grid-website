<template>
    <div>
        <h3>{{ edit.writer }}</h3>
        <h5>{{ edit.new }}</h5>
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