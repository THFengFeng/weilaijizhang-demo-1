<template>
    <div>
        <label class="formItem">
            <span class="name">{{this.fieldName}}</span>
            <input :placeholder="this.placeholder"
                   :value="value"
                   @input="onValueChanged($event.target.value)"
                   type="text">
        </label>
    </div>
</template>

<script lang="ts">
    import Vue from "vue";
    import {Component, Prop} from "vue-property-decorator";

    @Component
    export default class FormIte extends Vue {
        @Prop({default: ""}) readonly value!: string;
        @Prop({required: true}) fieldName!: string;
        @Prop() placeholder?: string;


        onValueChanged(value: string) {
            this.$emit("update:value", value);
        }
    }
</script>

<style lang="scss" scoped>
    .formItem {
        font-size: 14px;
        background: #f5f5f5;
        padding-left: 16px;
        display: flex;
        align-items: center;

        .name {
            padding-right: 16px;
        }

        input {
            height: 40px;
            flex-grow: 1;
            background: transparent;
            border: none;
            padding-right: 16px;
        }
    }
</style>
