<template>
  <div class="common-layout">
    <img alt="Vue logo" src="../assets/logo.png">
    <el-input v-model="input" placeholder="password"></el-input>
    <el-button @click="handle_click" type="success">enter</el-button>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data(){
    return{
      msg:'hello world!',

      input: ''
    }
  },methods:{
    handle_click() {
      const _this=this
      const url = "http://10.26.142.228:8181/changeBack?password=" + _this.input;
      axios.get(url).then(function (resp){
        alert(resp.data)
      })
    }
  },
  created() {

  }
}
</script>
<style scoped>

img {
  margin: 0 auto;
  align-items: center;
  text-align: center;
  display: flex;
}

</style>