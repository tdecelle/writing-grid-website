<template>
    <div class="homepage">
        <h1>Writing Grid</h1>
        <img alt="Writing Grid logo" height="300" src="../assets/writing-icon.png">
        <h2>Write - Edit - Connect</h2>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Homepage extends Vue {}
</script>

<style scoped>
    h1 {
        color: #1e5917;
        font-size: 30pt;
    }

    img {
        padding: 20px;
    }
</style>
