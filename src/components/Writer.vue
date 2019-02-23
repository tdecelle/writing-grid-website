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
    margin: 0px 300px 0px 300px;
    background-color: #4fc14d;
}

</style>