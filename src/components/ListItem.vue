<template>
    <div class="back">
        <Writer v-if="type.toLowerCase() == 'writer'" :writer="item"/>
        <Edit v-else-if="type.toLowerCase() == 'edit'" :edit="item"/>
        <Listing v-else-if="type.toLowerCase() == 'listing'" :listing="item"/>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';
    import Writer from '@/components/Writer.vue';
    import Edit from '@/components/Edit.vue';
    import Listing from '@/components/Listing.vue';


    @Component({
        components: {
            Writer,
            Edit,
            Listing,
        },
    })

    export default class ListItem extends Vue {
        @Prop() private type!: string;
        @Prop() private item!: object;
    }
</script>

<style scoped>
    .back {
        background-color: white;
        border-radius: 25px;
        margin: 10px;
        padding: 10px;
    }
</style>
