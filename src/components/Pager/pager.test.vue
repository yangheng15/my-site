<template>
    <div id="app">
        <Pager :current="current" :total="300" :limit="10" :visibleNumber="10" @pageChange="pageChange" />
    </div>
</template>

<script>
import Pager from './';
export default {
    name: 'App',
    components: {
        Pager,
    },
    data() {
        return {
            current: 10,
        };
    },
    methods: {
        pageChange(newPage) {
            console.log('页面改变', newPage);
            this.current = newPage;
        },
    },
};
</script>

<style scped>
.icon-container {
    font-size: 26px;
    color: red;
}
</style>
