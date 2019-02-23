<template>
    <div class="writer">
        <img :src=writer.imgurl alt="Writer's profile picture.">
        <h2>{{ writer.name }} </h2>
        <h4>{{ writer.title }}</h4>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Writer extends Vue {
        @Prop() private writer!: object;
    }
</script>

<style scoped>
    .writer {
        text-decoration:none;
        text-align:left;
        width: 100%;
    }

    img {
        height: 50px;
        width: 50px;
        border-radius: 50%;
        float: left;
        margin: 10px;
    }
</style>
