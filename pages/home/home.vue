<template>
  <view>
      <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true">
        <swiper-item v-for="(item, i) in swiperList" :key="i">
          <view class="swiper-item">
            <image :src="item.image_src"></image>
          </view>
        </swiper-item>
      </swiper>
    </view>
</template>

<script>
  export default {
    data() {
      return {
        swiperList: [
          {
            "id": 1,
            "image_src": "/static/swiperList/1.jpg",
          },
          {
            "id": 2,
            "image_src": "/static/swiperList/2.jpg",
          },
        ],
      }
    }
  }
</script>

<style lang="scss">
swiper {
 height: 330rpx;

 .swiper-item,
 image {
   width: 100%;
   height: 100%;
 }
}
</style>
