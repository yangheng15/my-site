<template>
    <div class="image-loader-container">
        <img v-if="isAllDone" class="placeholder" :src="placeholder" alt="" />
        <img @load="imageLoaded" class="origin" :src="src" :style="{ opacity: opacity, transition: duration }" />
    </div>
</template>

<script>
export default {
    props: {
        src: {
            type: String,
            required: true,
        },
        placeholder: {
            type: String,
            required: true,
        },
        duration: {
            type: Number,
            default: 500,
        },
    },
    data() {
        return {
            isimageLoaded: false,
            isAllDone: true,
        };
    },
    computed: {
        opacity() {
            return this.isimageLoaded ? 1 : 0;
        },
    },
    methods: {
        imageLoaded() {
            this.isimageLoaded = true;
            setTimeout(() => {
                this.isAllDone = false;
                this.$emit('load')
            }, this.duration);
        },
    },
};
</script>

<style lang="less" scoped>
@import url('~@/styles/mixin.less');
.image-loader-container {
    position: relative;
    border: 1px solid #000;
    width: 100%;
    height: 100%;
    overflow: hidden;
    .placeholder {
        filter: blur(2vw);
    }
    .origin {
        opacity: 0;
    }
    img {
        .self-fill();
        object-fit: cover;
    }
}
</style>
