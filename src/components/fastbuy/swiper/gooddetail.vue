<template>
  <!-- 选中商品之后进行加减 -->
  <div class="swiper_good_detail">
    <div class="swiper_good_detail_operation">
      <div class="swiper_good_detail_operation_add" @click="add"></div>
      <div class="swiper_good_detail_operation_mid">
        <div class="swiper_good_detail_operation_mid_sure">确认数量</div>
        <div class="swiper_good_detail_operation_mid_num">购买数量{{this.item[0].num}}</div>
      </div>
      <div class="swiper_good_detail_operation_descrease" @click="descrease"></div>
    </div>
  </div>
</template>
<script>
  export default {
    props: {
      item: {
        type: Array
      }
    },
    methods: {
      add() {
        console.log(this.item);
        this.item[0].num ++;
        console.log(this.item[0].num);
      },
      descrease() {
        if (this.item[0].num > 0) {
          this.item[0].num --;
          console.log(this.item[0].num);
        }
      }
    }
  };
</script>

<style>
  .swiper_good_detail{
    position: absolute;
    z-index: 999;
    top: -1.70rem;
    left: 0.1rem;
    width: 2.9rem;
    height: 1.69rem;
    font-size: 0.16rem;
    line-height: 0.3rem;
    color: white;
    background: yellow;
    background: url("../../../img/good.png") no-repeat;
    background-size: 100% 100%;
  }
  .swiper_good_detail_operation{
    margin-top: 1.13rem;
    height: 0.56rem;
    background: rgba(231, 46, 60, 0.8);
  }
  .swiper_good_detail_operation_add{
    float: left;
    width: 0.48rem;
    height: 0.55rem;
    background: url("../../../img/add.png") no-repeat;
    background-size: 100% 100%;
  }
  .swiper_good_detail_operation_mid{
    float: left;
    width: 1.92rem;
  }
  .swiper_good_detail_operation_mid_sure{
    border-bottom: 0.01rem solid #a50000;
  }
  .swiper_good_detail_operation_descrease{
    float: right;
    width: 0.49rem;
    height: 0.55rem;
    background: url("../../../img/descrease.png") no-repeat;
    background-size: 100% 100%;
  }
</style>
