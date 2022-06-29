<template>
  <div>
    <p>商品总数 {{ count }}</p>
    <button v-on:click="count++">+1</button>
    <button v-on:click="addFn">+1</button>
    <button v-on:click="addFn1(5)">+5</button>
    <button @click="subFn">-1</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    // 格式固定, 定义vue数据之处
    return {
      // key相当于变量名
      count: 0,
    };
  },
  methods: {
    // vue 的方法写在 里边
    addFn() {
      // this代表export default后面的组件对象(下属有data里return出来的属性)
      this.count++;
      // this 要注意一下
    },
    addFn1(val) {
      console.log(val);
      this.count += 5;
    },
    subFn() {
      this.count--;
    },
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
