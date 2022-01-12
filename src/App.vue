<template>
    <div id="app">
        <Avatar
            :size="50"
            url="https://img2.baidu.com/it/u=1685092271,2574681286&fm=253&fmt=auto&app=120&f=JPEG?w=1200&h=797"
        />
        <Icon type="home" />
        <Pager />
    </div>
</template>

<script>
import Avatar from "./components/Avatar.vue";
import Icon from "./components/Icon.vue";
import Pager from "./components/Pager.vue";
export default {
    name: "App",
    components: {
        Avatar,
        Icon,
        Pager,
    },
};
Promise.all();
</script>

<style scped>
.icon-container {
    font-size: 26px;
    color: red;
}
</style>
