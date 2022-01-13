<template>
    <div class="pager-container" v-if="pageNumber !== 0">
        <a :class="{ disable: current === 1 }" @click="handleClick(1)">|&lt;&lt;</a>
        <a :class="{ disable: current === 1 }" @click="handleClick(current - 1)">&lt;&lt;</a>
        <a v-for="(n, i) in numbers" :key="i" :class="{ active: n === current }" @click="handleClick(n)">{{ n }}</a>
        <a :class="{ disable: pageNumber === current }" @click="handleClick(current + 1)">&gt;&gt;</a>
        <a :class="{ disable: pageNumber === current }" @click="handleClick(pageNumber)">&gt;&gt;|</a>
    </div>
</template>

<script>
export default {
    props: {
        // 当前页码
        current: {
            type: Number,
            default: 1,
        },
        // 总的数据量
        total: {
            type: Number,
            default: 0,
        },
        // 一页的条数
        limit: {
            type: Number,
            default: 10,
        },
        visibleNumber: {
            type: Number,
            default: 10,
        },
    },
    computed: {
        // 总页数
        pageNumber() {
            return Math.ceil(this.total / this.limit);
        },
        // 得到现实最小的数字
        visibleMin() {
            let min = this.current - Math.floor(this.visibleNumber / 2);
            if (min < 1) {
                min = 1;
            }
            return min;
        },
        visibleMax() {
            let max = this.visibleNumber + this.visibleMin - 1;
            if (max > this.pageNumber) {
                max = this.pageNumber;
            }
            return max;
        },
        numbers() {
            const nums = [];
            for (let i = this.visibleMin; i <= this.visibleMax; i++) {
                nums.push(i);
            }
            return nums;
        },
    },
    methods: {
        handleClick(newPage) {
            if (newPage < 1) {
                newPage = 1;
            }
            if (newPage > this.pageNumber) {
                newPage = this.pageNumber;
            }
            if (newPage === this.current) {
                return;
            }
            this.$emit('pageChange', newPage);
        },
    },
};
</script>

<style lang="less" scoped>
@import '~@/styles/var.less';
.pager-container {
    display: flex;
    justify-content: center;
    margin: 20px 0;
    a {
        color: @primary;
        margin: 0 6px;
        cursor: pointer;
        &.disable {
            color: @lightWords;
            cursor: not-allowed;
        }
        &.active {
            color: @words;
            font-weight: bold;
            cursor: text;
        }
    }
}
</style>
