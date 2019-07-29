<template>
  <div class="header-swiper">

    


    <swiper :options="swiperOption">
      <!-- v-for="item in swiperList" :key:"item" -->
      <swiper-slide v-for="item in swiperList" :key="item.imgUrl">
        <img :src="item.imgUrl" />
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      swiperList: [
          {
            id: "01",
            imgUrl:
              "https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/a685001bbf5e77a203ff8815e953efbe.jpg_945x288_52b6ec01.jpg",
          },
          {
            id: "02",
            imgUrl:
              "https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/0677c297245b8a489ee12ab9b165c928.jpg_945x288_600cb364.jpg",
          },
          {
            id: "01",
            imgUrl:
              "https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/973dc1ae0da73a58410186df08ff25cb.jpg",
          },
          {
            id: "02",
            imgUrl:
              "https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/3f5ff03fa0c024b930f515e63ae2c702.jpg_945x288_7dff4510.jpg",
          }
        ],
      swiperOption: {
       
        pagination: {
          el: ".swiper-pagination"
        },
        loop: true
      }
    };
  }
};
</script>
<style scoped>
.header-swiper {
  background: #ccc;
  height: 0;
  padding-bottom: 26.67%
}

.header-swiper img {
  display: inline-block;
  width: 100%;
  height: 100%;
}

.header-swiper >>> .swiper-pagination-bullet-active {
  opacity: 1;
  background: #fff;
}
</style>
