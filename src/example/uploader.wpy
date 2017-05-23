<template>
    <view class="page">
        <view class="page__hd">
            <view class="page__title">Uploader</view>
            <view class="page__desc">上传组件</view>
        </view>
        <view class="page__bd">
            <view class="weui-cells">
                <view class="weui-cell">
                    <view class="weui-cell__bd">
                        <view class="weui-uploader">
                            <view class="weui-uploader__hd">
                                <view class="weui-uploader__title">图片上传</view>
                                <view class="weui-uploader__info">{{files.length}}/2</view>
                            </view>
                            <view class="weui-uploader__bd">
                                <view class="weui-uploader__files" id="uploaderFiles">
                                    <block wx:for="{{files}}" wx:key="*this">
                                        <view class="weui-uploader__file" @tap="previewImage" id="{{item}}">
                                            <image class="weui-uploader__img" src="{{item}}" mode="aspectFill" />
                                        </view>
                                    </block>
                                    <view class="weui-uploader__file">
                                        <image class="weui-uploader__img" src="../images/pic_160.png" mode="aspectFill" />
                                    </view>
                                    <view class="weui-uploader__file">
                                        <image class="weui-uploader__img" src="../images/pic_160.png" mode="aspectFill" />
                                    </view>
                                    <view class="weui-uploader__file">
                                        <image class="weui-uploader__img" src="../images/pic_160.png" mode="aspectFill" />
                                    </view>
                                    <view class="weui-uploader__file weui-uploader__file_status">
                                        <image class="weui-uploader__img" src="../images/pic_160.png" mode="aspectFill" />
                                        <view class="weui-uploader__file-content">
                                            <icon type="warn" size="23" color="#F43530"></icon>
                                        </view>
                                    </view>
                                    <view class="weui-uploader__file weui-uploader__file_status">
                                        <image class="weui-uploader__img" src="../images/pic_160.png" mode="aspectFill" />
                                        <view class="weui-uploader__file-content">50%</view>
                                    </view>
                                </view>
                                <view class="weui-uploader__input-box">
                                    <view class="weui-uploader__input" @tap="chooseImage"></view>
                                </view>
                            </view>
                        </view>
                    </view>
                </view>
            </view>
        </view>
    </view>
</template>

<script>
    import wepy from 'wepy';

    export default class Uploader extends wepy.page {

        data = {
            files: []
        };

        methods = {
            async chooseImage (e) {
                let res = await wepy.chooseImage({
                    sizeType: ['original', 'compressed'], // 可以指定是原图还是压缩图，默认二者都有
                    sourceType: ['album', 'camera'] // 可以指定来源是相册还是相机，默认二者都有
                });
                this.files = this.files.concat(res.tempFilePaths);
                this.$apply();
            },
            previewImage (e) {
                wepy.previewImage({
                    current: e.currentTarget.id, // 当前显示图片的http链接
                    urls: this.data.files // 需要预览的图片http链接列表
                });
            }
        }
    }
</script>
