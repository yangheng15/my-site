<template>
    <div id="app">
        <Empty text="暂无数据" />
    </div>
</template>

<script>
import Empty from './components/Empty';
export default {
    name: 'App',
    components: {
        Empty,
    },
    data() {
        return {};
    },
    methods: {},
};
</script>

<style scped>
/* .icon-container {
    font-size: 26px;
    color: red;
} */
</style>
