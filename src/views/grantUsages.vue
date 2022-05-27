<template>
  <div class="common-layout">
    <img alt="Vue logo" src="../assets/logo.png">
    <el-input v-model="input" placeholder="userName"></el-input>
    <el-button @click="handle_click" type="success">search</el-button>
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
      const url = "http://10.26.142.228:8181/grantUsages?userName=" + _this.input;
      axios.get(url).then(function (resp){
        alert(resp.data)
      })
    }
  },
  created() {

  }
}
</script>