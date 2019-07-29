<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(item,index) in mypage" :key="index">
        <div class="icons-item" v-for="page in item" :key="page.id">
          <img :src="page.imgUrl" alt />
          <p>{{page.title}}</p>
        </div>
      </swiper-slide>

    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      swiperOption: {
      },
      iconsList: [
        {
          id: "01",
          title: "景点门票",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "02",
          title: "必有榜单",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "03",
          title: "夏日玩水",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "04",
          title: "主题乐园",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "05",
          title: "动植物园",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "06",
          title: "故宫",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "07",
          title: "一日游",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "08",
          title: "公园",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "09",
          title: "游乐场",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        },
        {
          id: "10",
          title: "全部玩乐",
          imgUrl: "http://s.qunarzz.com/homenode/images/touchheader/hotel.png"
        }
      ],

    };
  },
  computed: {
    mypage() {
      console.log("hhhh")
      let pages = [];
      this.iconsList.forEach((item, index) => {
        console.log("hhhh")
        let idx = Math.floor(index/ 8);
        if (!pages[idx]) pages[idx] = [];
        pages[idx].push(item);
      });
      return pages;
    }
  }
};
</script>

<style scoped>
.icons-item {
  width: 25%;
  margin-top: 15px;
  padding-bottom: 25%;
  height: 0;
  /* background: #ccc; */
  float: left;
}

.icons-item img {
  width: 1.1rem;
  height: 1.1rem;
  display: block;
  margin: 0 auto;
  padding-top: 0.2rem;
}

.icons-item p {
  margin-top: 0.2rem;
  font-size: 0.28rem;
  text-align: center;
  color: #212121;
}

.header-swiper >>> .swiper-pagination-bullet-active {
  opacity: 1;
  background: #fff;
}
</style>
