<template>
  <view class="demo-swiper">
    <demo-block title="切换效果-淡入">
      <z-swiper v-model="list" :options="options">
        <z-swiper-item v-for="(item, index) in list" :key="index">
          <image class="image" :src="item" mode="aspectFill" />
        </z-swiper-item>
      </z-swiper>
    </demo-block>
    <demo-block title="自动播放">
      <z-swiper v-model="list" :options="optionsAutoplay">
        <z-swiper-item v-for="(item, index) in list" :key="index">
          <image class="image" :src="item" mode="aspectFill" />
        </z-swiper-item>
      </z-swiper>
    </demo-block>
    <demo-block title="纵向">
      <z-swiper
        v-model="list"
        :custom-style="{ height: '300rpx' }"
        :options="optionsVertical"
      >
        <z-swiper-item v-for="(item, index) in list" :key="index">
          <image class="image" :src="item" mode="aspectFill" />
        </z-swiper-item>
      </z-swiper>
    </demo-block>
    <demo-block title="无限循环">
      <z-swiper v-model="loopList" :options="optionsLoop">
        <z-swiper-item v-for="(item, index) in loopList" :key="index">
          <image class="image" :src="item" mode="aspectFill" />
        </z-swiper-item>
      </z-swiper>
    </demo-block>
  </view>
</template>

<script>
import DemoBlock from "../../components/DemoBlock/DemoBlock.vue";
export default {
  components: {
    DemoBlock,
  },
  data() {
    return {
      options: {
        effect: "fade",
        fadeEffect: {
          crossFade: true,
        },
      },
      optionsAutoplay: {
        effect: "fade",
        fadeEffect: {
          crossFade: true,
        },
        autoplay: true,
      },
      optionsVertical: {
        effect: "fade",
        fadeEffect: {
          crossFade: true,
        },
        direction: "vertical",
      },
      optionsLoop: {
        effect: "fade",
        fadeEffect: {
          crossFade: true,
        },
        loop: true,
      },
      list: [
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe4.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe5.jpg",
      ],
      loopList: [
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe4.jpg",
        "https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe5.jpg",
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.demo-swiper {
  .image {
    height: 300rpx;
    width: 100%;
  }
}
</style>
