<template>
  <div class="my-goods-item">
    <div class="left">
      <div class="custom-control custom-checkbox">
        <!-- *重要:
          每个对象和组件都是独立的
          对象里的goods_state关联自己对应商品的复选框
         -->
        <!-- bug:
          循环的所有label的for都是input, id也都是input - 默认只有第一个生效
          解决: 每次对象里的id值(1, 2), 分别给id和for使用即可区分
          -->
        <input type="checkbox" class="custom-control-input" :id="gObj.id" v-model="gObj.goods_state">
        <label class="custom-control-label" :for="gObj.id">
          <img :src="gObj.goods_img" alt="">
        </label>
      </div>
    </div>
    <div class="right">
      <div class="top">{{ gObj.goods_name }}</div>
      <div class="bottom">
        <span class="price">¥ {{ gObj.goods_price }}</span>
        <span>
          <MyCount :obj="gObj"></MyCount>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>