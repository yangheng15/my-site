<template>
    <div id="app">
        <div class="test-container">
            <Empty text="暂无数据"/>
        </div>
    </div>
</template>

<script>
import Empty from './';
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
.test-container {
    width: 500px;
    height: 400px;
    border: 1px solid #ccc;
    position: relative;
}
</style>
