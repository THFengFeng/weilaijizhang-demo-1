<template>
    <Layout class-prefix="layout">
        <NumberPad/>
        <Types :xxx="    333     "/>
        <Notes/>
        <Tags :data-source.sync="tags"/>
    </Layout>
</template>

<script>
    import NumberPad from '@/components/Money/NumberPad.vue'
    import Types from '@/components/Money/Types.vue'
    import Notes from '@/components/Money/Notes.vue'
    import Tags from '@/components/Money/Tags.vue'

    export default {
        name: 'Money',
        components: {Tags, Notes, Types, NumberPad},
        data() {
            return {
                tags:  ['衣服','食物','房租','交通',
                        '彩票','水费','电费','燃气',
                        '快递','健身','逛街','礼物']
            }
        }
    }
</script>

<style lang="scss">
    .layout-content {
        display: flex;
        flex-direction: column-reverse;
    }
</style>