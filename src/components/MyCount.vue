<template>
  <div class="my-counter">
    <button type="button" class="btn btn-light" >-</button>
    <input type="number" class="form-control inp" v-model.number="obj.goods_count">
    <button type="button" class="btn btn-light" >+</button>
  </div>
</template>

<script>
export default {
  props: {
    obj: Object // 商品对象
  }
}
</script>
