<template>
    <ul class="contact-container">
        <li>
            <a href="">
                <div class="icon">
                    <Icon type="github" />
                </div>
                <span>DuYi-Edu</span>
            </a>
        </li>
        <li>
            <a href="mailto:23423424234@qq.com">
                <div class="icon">
                    <Icon type="mail" />
                </div>
                <span>23423424234@qq.com</span>
            </a>
        </li>
        <li>
            <a
                href="tencent://message/?Menu=yes&uin=3263023350&Service=300&sigT=45a1e5847943b64c6ff3990f8a9e644d2b31356cb0b4ac6b24663a3c8dd0f8aa12a595b1714f9d45"
            >
                <div class="icon">
                    <Icon type="qq" />
                </div>
                <span>3263023350</span>
            </a>
            <div class="pop">
                <img src="http://www.duyiedu.com/source/img/%E5%85%AC%E4%BC%97%E5%8F%B7%E4%BA%8C%E7%BB%B4%E7%A0%81.png" alt="" />
            </div>
        </li>
        <li>
            <a>
                <div class="icon weixin">
                    <Icon type="weixin" />
                </div>
                <span>dsfggasas</span>
            </a>
            <div class="pop">
                <img src="http://www.duyiedu.com/source/img/%E5%85%AC%E4%BC%97%E5%8F%B7%E4%BA%8C%E7%BB%B4%E7%A0%81.png" alt="" />
            </div>
        </li>
    </ul>
</template>

<script>
import '@/styles/global.less';
export default {};
</script>

<style lang="less" scoped>
@import url(~@/styles/var.less);
.contact-container {
    padding: 20px;
    margin: 0;
    color: @gray;
    @itemHeight: 30px;
    li {
        height: @itemHeight;
        line-height: @itemHeight;
        position: relative;
        &:hover {
            .pop {
                transform: scaleY(1);
            }
        }
    }
    a {
        cursor: pointer;
        display: flex;
        align-items: center;
        font-size: 14px;
    }
    .icon {
        font-size: 26px;
        width: 36px;
        &.weixin {
            font-size: 32px;
            text-indent: -3px;
        }
    }
    .pop {
        position: absolute;
        left: 0;
        bottom: @itemHeight + 5px;
        transform: scaleY(0);
        transition: 0.3s;
        background-color: #fff;
        padding: 10px 15px;
        transform-origin: center bottom;
        border-radius: 15px;
        img {
            width: 150px;
            height: 150px;
        }
        &::after {
            content: '';
            width: 8px;
            height: 8px;
            background-color: #fff;
            position: absolute;
            bottom: -4px;
            left: 50%;
            transform: translateX(-50%) rotate(45deg);
        }
    }
}
</style>
