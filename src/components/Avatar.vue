<template>
  <img
    class="avatar-container"
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
<<<<<<< HEAD
.avatar-container {
  border-radius: 50%;
  object-fit: cover;
=======
.avatar-img {
    border-radius: 50%;
    object-fit: cover;
>>>>>>> 91c158b43b63c27589608a3917d98e6325f16db3
}
</style>
