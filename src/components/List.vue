<template>
    <div>
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

</style>