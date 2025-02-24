<template>
  <div class="hello">
<input type="text" v-model="username">
<input type="text" v-model.lazy.trim="password">
<p>{{ username }},{{ password }}</p>
<button @click="clickGetUsername">获取用户名与密码</button>
  </div>

</template>

<script>
import { withScopeId } from 'vue';

export default {
  name: 'HelloWorld',
  //表单输入绑定：可以根据v-model指令，实现对用户输入数据的监听并实现监听数据的更新
  //修饰符lazy:添加lazy修饰符后，在change事件触发后才进行数据更新（回车之后）
  //trim:使用后可以自动过滤掉用户输入的首尾空格
  data()
  {
    return{
      username:"",
      password:""
    }
  },
  methods:{
    clickGetUsername()
    {
      this.username="我就喜欢索萌"
      this.password="我超级喜欢索萌"
    }
  }
}
</script>

