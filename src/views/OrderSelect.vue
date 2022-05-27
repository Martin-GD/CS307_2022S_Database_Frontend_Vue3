<template>
  <img alt="Vue logo" src="../assets/logo.png">
  <div class="common-layout">
    <el-input v-model="contract_id" placeholder="contract_id"></el-input>
    <el-input v-model="model_id" placeholder="model_id"></el-input>
    <el-input v-model="salesman_id" placeholder="salesman_id"></el-input>
    <el-button @click="handle_click" type="success">search</el-button>

    <el-table :data="tableData"  align="center" stripe="true">
      <el-table-column prop="contract_id" label="contract_id" width="200" />
      <el-table-column prop="model_id" label="model_id" width="200" />
      <el-table-column prop="quantity" label="quantity" width="200" />
      <el-table-column prop="salesman" label="salesman" width="200" />
      <el-table-column prop="delivery_date" label="delivery_date" width="200" />
      <el-table-column prop="lodgement_date" label="lodgement_date" width="200" />
      <el-table-column prop="contract_type" label="contract_type" width="200" />
    </el-table>

  </div>
</template>

<script>
import axios from 'axios'

export default {
  data(){
    return{
      msg:'hello world!',
      tableData : [],

      contract_id: '',
      model_id:'',
      salesman_id:''
    }
  },methods:{
    handle_click() {
      const _this=this
      const url = "http://10.26.142.228:8181/OrderSelect?contract_id=" + _this.contract_id+"&model_id="+_this.model_id+"&salesman_id="+_this.salesman_id;
      axios.get(url).then(function (resp){
        _this.tableData = resp.data

        console.log(resp.data)
      })
      _this.contract_id=''
      _this.model_id=''
      _this.salesman_id=''
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