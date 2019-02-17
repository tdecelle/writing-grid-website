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
    background-color: cadetblue;
}

</style>