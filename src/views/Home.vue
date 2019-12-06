<template>
  <div class="home">
    <div class="main">
      <van-swipe :autoplay="2000" indicator-color="lime">
        <van-swipe-item>
          <img src="//dummyimage.com/100x100" alt />
        </van-swipe-item>
        <van-swipe-item>
          <img src="//dummyimage.com/100x100" alt />
        </van-swipe-item>
        <van-swipe-item>
          <img src="//dummyimage.com/100x100" alt />
        </van-swipe-item>
        <van-swipe-item>
          <img src="//dummyimage.com/100x100" alt />
        </van-swipe-item>
        <van-swipe-item>
          <img src="//dummyimage.com/100x100" alt />
        </van-swipe-item>
      </van-swipe>
      <div class="navList">
        <dl v-for="item in list" :key="item.id">
          <dt>
            <img :src="item.img" alt />
          </dt>
          <dd>{{item.title}}</dd>
        </dl>
      </div>
      <div class="content">
          <img src="//dummyimage.com/200x100" alt="" v-for="n in 4" :key="n">
      </div>
    </div>
    <TabBar></TabBar>
  </div>
</template>

<script>
import Vue from "vue";
import { Swipe, SwipeItem } from "vant";
Vue.use(Swipe).use(SwipeItem);
export default {
  name: "home",
  data() {
    return {
      list: [
        {
          id: 0,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        },
        {
          id: 1,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        },
        {
          id: 2,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        },
        {
          id: 3,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        },
        {
          id: 4,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        },
        {
          id: 5,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        },
        {
          id: 6,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        },
        {
          id: 7,
          img: "//dummyimage.com/50x50",
          title: "绩效考核"
        }
      ]
    };
  },
  components: {}
};
</script>

<style lang="scss">
.content{
  width: 100%;display: flex;
  overflow-x: scroll;
  img{
    flex-shrink: 0;
    margin: 0 10px;
  }
}
.main {
  width: 100%;
  height: 617px;
  overflow: auto;
}
.van-swipe {
  width: 100%;
  height: 200px;
  margin-top: 20px;
  img {
    width: 100%;
  }
}
.navList {
  width: 100%;
  height: 200px;
  display: flex;
  flex-wrap: wrap;
  margin-top: 20px;
  dl {
    width: 25%;
    text-align: center;
    img {
      border-radius: 50%;
    }
  }
}
</style>
