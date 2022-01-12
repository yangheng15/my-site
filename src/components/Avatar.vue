<template>
    <img
        class="avatar-img"
        :src="url"
        :style="{ width: size + 'px', height: size + 'px' }"
    />
</template>

<script>
export default {
    props: {
        url: {
            type: String,
            required: true,
            default: "",
        },
        size: {
            type: Number,
            default: 50,
        },
    },
    methods: {
        test() {},
    },
};
</script>

<style lang="less" scoped>
.avatar-img {
    border-radius: 50%;
    object-fit: cover;
}
</style>
