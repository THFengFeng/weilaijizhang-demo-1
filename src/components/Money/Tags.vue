@@ -1,7 +1,7 @@
<template>
    <div class="tags">
        <div class="new">

            <button @click="create">新增标签</button>
        </div>
        <ul class="current">
            <li :class="{selected: selectedTags.indexOf(tag)>=0}" :key="tag"
                @click="toggle(tag)"
                v-for="tag in dataSource">{{tag}}
            </li>
        </ul>
    </div>
</template>

<script lang="ts">

</script>

<style lang="scss" scoped>
    .tags {
        font-size: 14px;
        padding: 16px;
        flex-grow: 1;
        display: flex;
        flex-direction: column-reverse;

        > .current {
            display: flex;
            flex-wrap: wrap;

            > li {
                background: #d9d9d9;
                $h: 24px;
                height: $h;
                line-height: $h;
                border-radius: $h/2;
                padding: 0 16px;
                margin-right: 12px;
                margin-top: 4px;
            }
        }

        > .new {
            padding-top: 16px;

            button {
                background: transparent;
                border: none;
                color: #999;
                border-bottom: 1px solid;
                padding: 0 4px;
            }
        }
    }

    </style>