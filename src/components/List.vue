<template>
    <div class="list">
        <h1>{{ name }}</h1>
        <ListItem :key="item" v-for="item in json" :type=type :item="item" />
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';
    import ListItem from '@/components/ListItem.vue';

    @Component({
        components: {
            ListItem,
        },
    })

    export default class List extends Vue {
        @Prop() private name!: string;
        @Prop() private type!: string;
        @Prop() private json!: object;
    }
</script>

<style scoped>
    .list{
        background-color: #b7b7b7;
        border-radius: 25px;
        /*border: 2px solid black;*/
        padding: 10px;
        margin: 10px;
    }
</style>