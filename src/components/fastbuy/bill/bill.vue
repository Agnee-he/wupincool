//拿发票组件
<template>
  <div class="bill">
    <div class="bill_tab">
      <router-link class="tab_item" to="/fastbuy"><</router-link>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        showBill: false
      };
    },
    methods: {
      show() {
          this.showBill = true;
      },
      hideBill() {
          this.showBill = false;
      }
    }
  };
</script>

<style>
  .bill{
    position: fixed;
    z-index: 10;
    left: 0;
    top: 0;
    bottom: 63px;
    z-index: 30;
    width: 100%;
    background: #fff;
  }
  .bill_tab{
    position: relative;
  }
  .bill_tab .tab_item{
    position: absolute;
    line-height: 16px;
    left: 10px;
    top: 10px;
  }
</style>
