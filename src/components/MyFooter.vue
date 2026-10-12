<template>
  <!-- 底部 -->
  <div class="my-footer">
    <!-- 全选 -->
    <div class="custom-control custom-checkbox">
      <input type="checkbox" class="custom-control-input" id="footerCheck" v-model="isAll">
      <label class="custom-control-label" for="footerCheck">全选</label>
    </div>
    <!-- 合计 -->
    <div>
      <span>合计:</span>
      <span class="price">¥ {{ allPrice }}</span>
    </div>
    <!-- 按钮 -->
    <button type="button" class="footer-btn btn btn-primary">结算 ( {{ allCount }} )</button>
  </div>
</template>

<script>
// 目标: 全选
// 1. v-model关联全选-复选框(v-model后变量计算属性)
// 2. 页面(视频层)v(true) -> 数据层(变量-) 计算属性(完整写法)
// 3. 把全选 true/false同步给所有小选框选中状态上

// 小选  -> 全选
// App.vue里list数组 -> MyFooter.vue
// isAll的get方法里, 统计状态影响全选框

// 目标: 总数量统计
// 1. allCount计算属性用 数组reduce+判断统计数量并返回

// 目标: 总价
// allPrice计算属性, 数组reduce+单价*数量, 判断选中, 才累加后返回

export default {

}
</script>