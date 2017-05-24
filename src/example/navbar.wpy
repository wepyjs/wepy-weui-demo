<style lang="less">
.navbar {
    .page,
    .page__bd{
        height: 100%;
    }
    .page__bd{
        padding-bottom: 0;
    }
    .weui-tab__content{
        padding-top: 60px;
        text-align: center;
    }
}
</style>
<template>
    <view class="navbar page">
        <view class="page__bd">
            <view class="weui-tab">
                <view class="weui-navbar">
                    <view wx:for="{{tabs}}" wx:key="*this" id="{{index}}" class="weui-navbar__item {{activeIndex == index ? 'weui-bar__item_on' : ''}}" @tap="tabClick">
                        <view class="weui-navbar__title">{{item}}</view>
                    </view>
                    <view class="weui-navbar__slider" style="left: {{sliderLeft}}px; transform: translateX({{sliderOffset}}px); -webkit-transform: translateX({{sliderOffset}}px);"></view>
                </view>
                <view class="weui-tab__panel">
                    <view class="weui-tab__content" hidden="{{activeIndex != 0}}">选项一的内容</view>
                    <view class="weui-tab__content" hidden="{{activeIndex != 1}}">选项二的内容</view>
                    <view class="weui-tab__content" hidden="{{activeIndex != 2}}">选项三的内容</view>
                </view>
            </view>
        </view>
    </view>
</template>

<script>
    import wepy from 'wepy';

    const sliderWidth = 96; // 需要设置slider的宽度，用于计算中间位置

    export default class Toast extends wepy.page {

        data = {
            tabs: ['选项一', '选项二', '选项三'],
            activeIndex: 1,
            sliderOffset: 0,
            sliderLeft: 0
        };

        methods = {
            tabClick (e) {
                this.sliderOffset = e.currentTarget.offsetLeft;
                this.activeIndex = e.currentTarget.id;
            }
        }

        async onLoad () {
            let res = await wepy.getSystemInfo();

            this.sliderLeft = (res.windowWidth / this.tabs.length - sliderWidth) / 2;
            this.sliderOffset = res.windowWidth / this.tabs.length * this.activeIndex;
        }
    }
</script>
