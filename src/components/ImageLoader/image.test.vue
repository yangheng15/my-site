<template>
    <div id="app">
        <ImageLoader
            src="https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?fit=crop&crop=entropy&w=3456&h=2304"
            placeholder="https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?w=100"
            @load="handleLoaded"
            
        />
    </div>
</template>

<script>
import ImageLoader from './';
export default {
    name: 'App',
    components: {
        ImageLoader,
    },
    data() {
        return {};
    },
    methods: {
        handleLoaded() {
            console.log('加载完了');
        }
    },
};
</script>

<style scped>
#app {
    /* width: 500px; */
    height: 100vh;
    /* margin: 0 auto; */
}
</style>
