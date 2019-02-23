<template>
    <div class="writer">
        <h3>{{ name }}</h3>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Writer extends Vue {
        @Prop() private name!: string;
    }
</script>

<style scoped>

.writer {
    margin: 0px 300px 0px 300px;
    background-color: #4fc14d;
}

</style>