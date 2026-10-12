<template>
  <div>
    <MyHeader/>
    <MyGoods/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyFooter from './components/MyFooter.vue';
import MyGoods from './components/MyGoods.vue';
export default {
    components: { MyHeader, MyFooter, MyGoods }
}
</script>

<style>

</style>
