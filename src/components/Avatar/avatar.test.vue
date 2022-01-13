<template>
    <div id="app">
        <Avatar :size="50" url="https://img2.baidu.com/it/u=1685092271,2574681286&fm=253&fmt=auto&app=120&f=JPEG?w=1200&h=797" />
    </div>
</template>

<script>
import Avatar from './components/Avatar/index.vue';
export default {
    name: 'App',
    components: {
        Avatar,
    },
    data() {
        return {};
    },
    methods: {},
};
</script>

<style scped>
.icon-container {
    font-size: 26px;
    color: red;
}
</style>
