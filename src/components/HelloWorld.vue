<template>
  <div class="hello">
    <h1>{{ name }}</h1>
    <h2></h2>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component({ name: "Hello" })
export default class Hello extends Vue {
  private name: string = "张三";
  private sex: string = "男";

  setName(val: string = "测试数据") {
    console.log(val);
  }

  mounted() {
    this.setName();
  }
}
</script>
<style lang="less" scoped></style>
