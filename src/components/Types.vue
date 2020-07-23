<template>

</template>

<script lang="ts">
    import Vue from "Vue";
    import {Component, Prop} from "vue-property-decorator";

    @Component
    export default class Types extends Vue {
        type = "-";                  // '-'表示支出. '+'表示收入
        @Prop(Number) xxx: number | undefined;

        selectType(type: string) {           //type 只能是'-'和'+'中的一个
            if (type !== "-" && type !== "+") {
                throw new Error("type is unknown");
            }
            this.type = type;
        }

        mountde() {
            console.log(this.xxx);
        }
    }


</script>

<style lang="scss" scoped>

</style>