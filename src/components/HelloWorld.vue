<template>
  <div class="hello">
      <v-child></v-child>
  </div>
</template>
<script lang="ts">
import { Component, Vue, Emit } from "vue-property-decorator";
import VChild from "./Child.vue";

@Component({ name: "Hello", components:{ VChild }})

export default class Hello extends Vue {

  setName(val: string = "测试数据测试") {
    console.log(val);
  }
  
  makeDetail(){
    const refs:any = this.$refs.age;
    console.log("当前节点：：",refs.innerHTML);
  }

  mounted() {
     
  }
}
</script>
<style lang="less" scoped>
   .hello{
      h1{
        cursor: pointer;
      }
   }
</style>
