<template>
    <div id="app">
        <Icon type="home" />
    </div>
</template>

<script>
import Icon from './components/Icon/index.vue';
export default {
    name: 'App',
    components: {
        Icon,
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
