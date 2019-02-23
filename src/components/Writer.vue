<template>
    <div class="writer">
        <img src="../assets/shrek.jpg" alt="Writer's profile picture.">
        <h2>{{ writer.first }}  {{ writer.last }}</h2>
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