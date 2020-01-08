<template>
  <view class="content">
    <image class="logo" src="/static/meeting.png" mode="aspectFill"></image>
    <view class="info">
      <view>北京市朝阳区金汇路9号中骏世界城D座B1层</view>
      <view>2020年1月16日 18:00 - 22:00</view>
      <button class="sign-up" open-type="getUserInfo" @getUserInfo="getUserInfo">立即报名</button>
      <!-- <uni-popup ref="popup" type="bottom">底部弹出 Popup</uni-popup> -->
      <view class="warning">请勿重复报名</view>
    </view>
  </view>
</template>

<script>
// import uniPopup from "@dcloudio/uni-ui/lib/uni-popup/uni-popup.vue";
export default {
//   components: {
//     uniPopup
//   },
  data() {
    return {};
  },
  onLoad() {},
  methods: {
    getUserInfo(info) {
    //   this.$refs.popup.open();
    console.log(info)
    }
  }
};
</script>

<style>
page {
  width: 100%;
  height: 100%;
}
.content {
  width: 100%;
  height: 100%;
  position: relative;

}
.logo {
  height: 100%;
  width: 100%;
}
.info {
  position: absolute;
  left: 50%;
  bottom: 2%;
  width: 100%;
  text-align: center;
  transform: translateX(-50%);
  color: #fff;
  font-size: 24upx;
}
.warning {
  font-size: 22upx;
  margin-top: 10upx;
}
.sign-up {
  background: transparent;
  width: 70%;
  color: #fff;
  margin-top: 40upx;
  border: 1upx solid rgba(255, 0, 0, 1);
}
</style>
