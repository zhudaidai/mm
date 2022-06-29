<template>
   <div @click="fatherFn">
   <!-- vue对事件进行了修饰符设置, 在事件后面.修饰符名即可使用更多的功能 -->
    <span @click.stop="one" href="http://www.baidu.com">.stop阻止事件冒泡</span>
    <br>
    <!-- href="http://www.baidu.com" -->
    <a @click.prevent.stop  href="http://www.baidu.com">.prevent阻止默认行为</a>
    <br>
    <button @click.once="btn">.once程序运行期间, 只触发一次事件处理函数</button>
  </div>
</template>

<script>


export default {
  data() { // 格式固定, 定义vue数据之处
    return {  // key相当于变量名
    
    }
      
  },
  methods: {
    fatherFn(){
      console.log("father被触发");
    },
    one () {
     console.log('span click');
    },
    btn(){
      console.log(1);
    }
  }
}
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
