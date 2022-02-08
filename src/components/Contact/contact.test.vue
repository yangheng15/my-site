<template>
    <div id="app">
        <Contact />
    </div>
</template>

<script>
import Contact from './';
export default {
    name: 'App',
    components: {
        Contact,
    },
    data() {
        return {};
    },
    methods: {},
};
</script>

<style scped>
#app {
    width: 400px;
    height: 400px;
    border: 2px solid red;
    background: #000;
    margin: 0 auto;
    padding-top: 200px;
}
</style>
