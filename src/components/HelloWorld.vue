<template>
  <div class="hello">
    {{ msg }}
    {{ 1+1 }}
    <div v-html="result"></div>
    <div v-bind:class="isActive">绑定事件</div>
    <p>{{ message.split('').reverse().join('') }}</p>
  <div>
    <p v-if="isFlag">我是齐天大圣s</p>
    <p v-else>我是齐天大圣</p>
  </div>
  <div>
    <ul>
      <li v-for="(item,index) in names " v-bind:key="index"> {{ item }}</li>
    </ul>
  </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'hello world App',
      result: '<h3>我是泰迪AAAA</h3>',
      isActive: 'actives',
      message: 'message',
      isFlag: false,
      names:["daiv","wang","li"]
    }
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
