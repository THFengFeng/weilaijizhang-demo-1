<template>
    <div class="layout-wrapper">
        <div :class="contentClass" class="content">
            <slot/>
        </div>
        <Nav/>
    </div>
</template>

<script lang="ts">
    export default {
        props: ["contentClass"],
        name: "Labels"
    };
</script>

<style lang="scss" scoped>
    .layout-wrapper {
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    .content {
        overflow: auto;
    }

</style>
